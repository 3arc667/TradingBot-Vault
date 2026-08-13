---
date: 2026-08-13
id: erreur-003
gravite: MAJEURE
type: Analyse
recurrence: 1ère fois
---

## 🚨 Description

J'ai validé une config copytrade TP 35% sur un « backtest » qui n'en était pas un :

- copy1 `E7T1Vs7a…` → **n = 9** tokens notés à la main
- copy2 `6GKHVwqR…` → **n = 7** tokens notés à la main

Conclusion tirée : ~85% de winrate, config rentable, activation.

## 🔍 Cause racine

### 1. Échantillon non significatif

À n = 7-9, un taux observé de 85% est statistiquement indiscernable de 50%. Ce n'est pas un backtest, c'est un relevé.

### 2. Biais de sélection

Je note les tokens que je remarque, pas tous ceux où le wallet achète. Les entrées mortes ne sont jamais saisies.

**Preuve chiffrée (MCP Fproject) :**

| Wallet | Mon journal | Fproject (50 derniers) |
|--------|-------------|------------------------|
| copy2 | 6/7 = 86% | **31/50 = 62%** |
| copy1 | 8/9 = 89% | 46/50 = 92% |

Sur copy2 l'écart est de 24 points. Mon relevé surestime.

### 3. Bug de l'app « point d'entrée / ATH »

L'app est correcte sur les tokens qui montent :

| Token | Mon app | Fproject | Écart |
|-------|---------|----------|-------|
| GD758yot… | +55% | +58% | OK |
| GhNMkkRc… | +49% | +47% | OK |
| Yb4vUYbQ… | +100% | +98% | OK |
| **8eisWDF7…** | **-88%** | **pic +31%** | ❌ BUG |

**Bug A — plancher au lieu du pic.** Sur un token qui rug, l'app enregistre le prix final au lieu du pic atteint. Je rate mes quasi-TP et je fausse le winrate.

**Bug B — gain du dev au lieu du mien.** Vérifié sur `EjURSLP2…` : mon app affiche +275%, Fproject « depuis entrée dev » = +276% (match exact), mais **ajusté copytrade = +248%**. Mon app mesure le gain depuis le lancement, pas depuis mon entrée réelle. Sur copy1 le même écart atteignait 1000% → 100%, soit **10x**.

## 💸 Impact PnL

- **Montant perdu** : $0 sur ce point précis
- **Trades affectés** : configs activées sur base faussée (cf. C1)
- **Risque** : surestimation systématique de l'EV de toute stratégie validée par cette app

## ✅ Correction appliquée

1. **n ≥ 50 minimum** avant toute validation de config
2. Enregistrer le **pic post-entrée**, jamais le prix final
3. Enregistrer le gain depuis **mon entrée réelle**, pas depuis le lancement
4. Croiser systématiquement le relevé perso avec l'échantillon Fproject
5. Noter **chaque** signal, sans exception — y compris les morts

## 🔒 Vérification

- [ ] Fix app : pic au lieu du plancher
- [ ] Fix app : gain depuis entrée réelle
- [ ] Nouvelle règle ajoutée dans `REGLES-OR.md`
- [ ] Test en paper trading validé (n ≥ 50)
- [x] `erreurs-recurrentes.md` mis à jour

## 📎 Liens

- Stratégie : `03-STRATEGIES/strategie-copytrade-v1.md`
- Erreur liée : `06-ERREURS/erreur-004.md`
