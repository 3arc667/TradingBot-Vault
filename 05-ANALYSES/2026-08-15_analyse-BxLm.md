---
date: 2026-08-15
type: analyse-wallet
wallet: BxLmrDJaNr9hA35FBGASAhUK74Gs98AyvQXx6HSR1Qft
methode: copytrade (Method 2)
statut: PAPER — non activé
copytrade_score: 75
rugger_score: 83
source: desk Fproject (rapport wallet profond)
---

# Analyse wallet — BxLm…1Qft

## 1. Identité
- **Ring / bundler** financé par **KuCoin Hot Wallet 2** (CEX), montant 0.08646 SOL.
- 656 tokens tradés, 538 bundlés. Âge ~63j.
- Type technique : `atomic_relay` (forward vers 89Xz…gdb7). Le funding transite, mais les achats et la géométrie d'entrée sont réels → copiable.
- **Même ring que copy wallet 1 (E7T1Vs…)** : 5 tokens en commun, 10 co-occurrences récentes.

## 2. Qualité d'entrée (le seul critère qui compte en copy)
- **Block 0 sur ~99,7%** des entrées (652/654).
- Médiane d'entrée **+0 bloc**. Avg +16,4 (biaisé par outliers).
- Caveat desk : placement élite, mais **contention de landing** = le vrai risque en live.

## 3. Distribution ATH copytrade (base = close de bougie)
Échantillon : **60 tokens** (sous-ensemble top-ATH du rapport).
- Médiane **+121%**, moyenne +228%, min +35%, max +1837%.

| TP | Taux d'atteinte (réel sur l'échantillon) |
|---|---|
| +50%  | 95% (57/60) |
| +75%  | 73% (44/60) |
| +100% | 60% (36/60) |
| +150% | 42% (25/60) |
| +200% | 33% (20/60) |
| +300% | 15% (9/60) |

## 4. Simulation EV/trade (net frais ~6%, Lmiss = perte moyenne sur les ratés)

| TP | hit | Lmiss −30% | −60% | −100% |
|---|---|---|---|---|
| +50%  | 95% | +40% | +38% | **+36%** |
| +75%  | 73% | +41% | +33% | +22% |
| +100% | 60% | +42% | +30% | +14% |
| +150% | 42% | +39% | +21% | −2% |
| +200% | 33% | +41% | +21% | −6% |

Étagé (moitié/moitié) : **50/150 → EV +57%** · **50/200 → EV +61%**.

## 5. Limites (à ne pas oublier)
- ⚠️ **Biais de survivant** : les 60 tokens sont les meilleurs par ATH. Wallet complet = 656 tokens dont **533 rug**. → taux ci-dessus = **plafond**, pas la réalité. (cf. erreur-003)
- ⚠️ **Lmiss = hypothèse**, pas donnée. Pas de chemin de baisse par token. **Ce n'est pas un backtest validé.**
- Les TP hauts (+150/+200) ne paient que si les pertes sont contenues → fragiles.

## 6. Verdict
- Entrées élite confirmées, wallet copiable **en hypothèse**.
- Config la plus robuste au biais : **TP serré étagé 50/150**, position $50 max, ce wallet seul.
- **Statut : PAPER.** Gate vault : ≥20 lancements / ≥72h + 48h paper avant tout live.

→ Stratégie : `03-STRATEGIES/strategie-copytrade-BxLm-v1.md`
