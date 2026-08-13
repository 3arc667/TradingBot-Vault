---
date: 2026-08-13
id: erreur-002
gravite: MAJEURE
type: Analyse
recurrence: 1ère fois
---

## 🚨 Description

J'ai identifié trois « adresses mères que je connais déjà » finançant les tokens de mes wallets copytradés, et j'en ai fait un signal d'entrée :

- `5tzFkiKscXHK5ZXCGbXZxdw7gTjjD1mBwuoFbhUvuAi9`
- `BmFdpraQhkiDQE6SnfG5omcA1VwzqfXrwtNYBwWTymy6`
- `u6PJ8DtQuPFnfmwHbGFULQ4u4EgjDiyYKjVEsynXq2w`

Raisonnement erroné : « ces tokens sont fundés par des montants très précis et des adresses mères connues → pattern exploitable ».

## 🔍 Cause racine

**Données MCP Fproject :**

`5tzFkiKscXHK5ZXCGbXZxdw7gTjjD1mBwuoFbhUvuAi9` = **Binance Hot Wallet 2** — `kind: Centralized Exchange`

Ce n'est pas une mère privée. C'est un hot wallet d'exchange. Des centaines de milliers de wallets Solana en sortent. **Le funding depuis une adresse CEX ne porte aucune information discriminante.**

Mes deux wallets copytradés en viennent tous les deux — ce qui m'a fait croire à une corrélation alors que c'est la base statistique.

### La règle correcte (Méthode 1)

Le signal n'est **jamais** l'adresse CEX. C'est le **montant exact réutilisé**, filtre hair-thin ±0,0001, avec **≥ 2 siblings** au même montant.

- Sans siblings ≥ 2 → pas de signature → pas de pattern
- Bande large (±0,01) = sans valeur
- Enfant CEX one-shot sans frère = REJECT

### Vérification effectuée

| Wallet | Montant funding | Siblings au même montant |
|--------|-----------------|--------------------------|
| copy1 `E7T1Vs7a…` | 0,099 SOL | à re-vérifier (crawl profond requis) |
| copy2 `6GKHVwqR…` | 24,734 SOL | **0** sur 400 enfants crawlés |

→ Aucune signature réutilisable derrière copy2. Ce que j'ai pris pour un pattern était de la plomberie d'exchange.

## 💸 Impact PnL

- **Montant perdu** : $0 (détecté avant conclusion)
- **Trades affectés** : 0
- **Risque évité** : copytrade activé sur une fausse corrélation de funding

## ✅ Correction appliquée

1. Avant de traiter un funder comme signal → vérifier son `kind`
2. Si CEX → chercher **montant + siblings ≥ 2**, jamais l'adresse seule
3. Hair-thin ±0,0001 uniquement, jamais de bande large
4. copy2 désactivé

## 🔒 Vérification

- [ ] Nouvelle règle ajoutée dans `REGLES-OR.md`
- [x] Stratégie mise à jour (copy2 abandonné)
- [ ] Test en paper trading validé
- [x] `erreurs-recurrentes.md` mis à jour

## 📎 Liens

- Stratégie : `03-STRATEGIES/strategie-copytrade-v1.md`
- Ruggers : `02-RUGGERS/SCHEMAS-RUGGERS.md`
