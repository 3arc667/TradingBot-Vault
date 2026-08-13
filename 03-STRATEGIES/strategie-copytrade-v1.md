# 🎯 STRATÉGIE — Copytrade bundler block-0 — v1

> **STATUS : PAPER TRADING — NON VALIDÉE**

## 📋 Informations

- **Type de rugger** : Bundler / ring block-0 (nouveau type, pas A/B/C)
- **Version** : v1
- **Date de création** : 2026-08-13
- **Créée par** : Claude (analyse Fproject) + validation humaine en attente
- **Status** : TEST

## 🎯 Objectif

Copier les entrées block-0 de `E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH` avec sortie à TP fixe, sans hériter de son comportement de bagholding.

## 🔍 Cible — pourquoi celle-là

| Métrique Fproject | copy1 `E7T1Vs7a…` |
|-------------------|-------------------|
| copytrade_score | **75 / 100** |
| worth_copytrading | ✅ oui |
| rugger_score | 83 |
| Échantillon | **625 tokens / 60 j** |
| Placement | Block-0 sur **100%** des entrées, médiane +0 |
| Profil | Bundler (544 tokens), ring de 16 wallets co-fundés |
| Taille moyenne | ~20,5 SOL / trade |
| Hold moyen | 64 s |
| Fréquence récente | ~15 signaux / jour (106 tokens sur 7 j) |
| **Touche +35% (50 derniers, ajusté copytrade)** | **46/50 = 92%** |

## ⚙️ Configuration du bot

| Paramètre | Valeur | Justification |
|-----------|--------|---------------|
| Montant d'entrée | $50 | Règle d'or |
| Take Profit (TP) | 35% | Touché 92% du temps sur n=50 ajusté copytrade |
| Stop Loss (SL) | naturel (floor) | Les échecs sont des rugs, pas des drawdowns |
| Délai copy | 2 s | Valeur testée |
| Copytrade | OUI | `E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH` |

## 🧠 Thèse

Le PnL propre du wallet est négatif (**-154 SOL total**, réalisé +4350 / non réalisé -4505) mais **ça n'invalide pas la stratégie** : ce déficit vient de **476 sacs jamais vendus** sur 655 tokens.

Un TP dur à 35% n'hérite pas de ce comportement. Le bon indicateur n'est pas son PnL, c'est le **taux de touche ajusté copytrade = 92%**.

## ⚠️ VARIABLE NON MESURÉE — bloque la validation

**Le taux de remplissage du TP.**

Toucher +35% au pic ≠ vendre à +35%. Le pic peut durer quelques secondes. L'ordre doit atterrir dedans.

Fproject signale explicitement sur ce wallet : *« land contention is the real caveat »*.

C'est la seule variable qui décide si ce setup gagne ou perd, et je n'ai **aucune donnée** dessus.

## 🧪 Protocole paper 48 h

Mesurer **une seule métrique** :

```
taux_remplissage = (sorties effectives à +35%) / (fois où +35% a été touché)
```

Règles de saisie (cf. `erreur-003`) :
- Noter **chaque** signal, sans exception — y compris les morts
- Noter le **pic**, pas le prix final
- Noter le gain depuis **mon entrée réelle**, pas depuis le lancement
- Objectif : **n ≥ 50 signaux**

## 📊 Seuils de décision

| Taux de remplissage | Décision |
|---------------------|----------|
| > 70% | Passage réel envisageable, taille $50 |
| 50-70% | Re-tester TP abaissé, nouveau paper |
| < 50% | Abandon de la config |

## 🛡️ Calcul de risque

~15 signaux/jour × $50 = **~$750 d'exposition brute quotidienne**.

Stop journalier -$200 → **3 rugs pleins terminent la session**.
Avec 8% de taux d'échec observé, 3 rugs groupés sont **dans la variance normale** d'une journée.

→ Ne pas interpréter un stop touché comme un échec de la stratégie. C'est prévu par la structure.

## ⚠️ Conditions d'abandon

- [ ] Taux de remplissage < 50% sur 50 signaux
- [ ] Winrate réel < 40% sur 20 trades
- [ ] PnL cumulé < -$200
- [ ] Le wallet cible change de comportement (placement, taille, fréquence)

## 📊 Backtest / Résultats

| Date | Token | Résultat | PnL | Notes |
|------|-------|----------|-----|-------|
| | | | | *paper en cours* |

**Winrate réel** : —
**Taux de remplissage** : —
**Trades** : 0

## 📝 Notes et évolutions

### v1 — création
Issue de l'analyse Fproject du 2026-08-13. Le relevé manuel initial (n=9) est **non recevable** comme validation, cf. `erreur-003`.

---

> **RAPPEL** : Toute modification = nouvelle version + paper trading 48h

## ❌ Wallet écarté

`6GKHVwqRSuJa3UJ7VBDHmU6Kq1ZTw1uE5sffyBbARb5Z` (copy2) — **coupé**.
copytrade_score **0**, worth_copytrading **false**, 38 h d'âge, médiane d'entrée **+1144 blocks**, touche +35% seulement 62% du temps, 0 trade au-dessus de 2x réalisé. Entrée tardive sur momentum déjà parti.

## 📎 Liens

- `06-ERREURS/erreur-002.md` — funding CEX
- `06-ERREURS/erreur-003.md` — backtest non significatif
- `02-RUGGERS/SCHEMAS-RUGGERS.md`
