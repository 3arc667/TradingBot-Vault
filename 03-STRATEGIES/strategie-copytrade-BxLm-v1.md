---
strategie: copytrade-BxLm
version: v1
date_creation: 2026-08-15
wallet_cible: BxLmrDJaNr9hA35FBGASAhUK74Gs98AyvQXx6HSR1Qft
methode: copytrade (Method 2)
statut: 🟢 PAPER EN COURS (banc ring)
paper_start: 2026-08-15T22:15Z
paper_end: 2026-08-17T22:15Z
validation_humaine: en attente
---

# Stratégie copytrade — BxLm v1

> 🟡 **PAPER — NON ACTIVÉE.** Aucun capital réel. Gate : 48h paper + ≥20 lancements / ≥72h + validation humaine avant tout live.

> ⚠️ **REDONDANT avec E7T1Vs (même ring).** Géométrie d'entrée identique (block-0 99,7%). Copier les deux = 2 buys par lancement. **Référence retenue = E7T1Vs** (voir `strategie-copytrade-E7T1Vs-v1.md`). BxLm = backup équivalent, ne pas activer en parallèle. Réf. analyse : `05-ANALYSES/2026-08-15_analyse-ring-copytrade.md`.

## Cible
- Wallet : `BxLmrDJaNr9hA35FBGASAhUK74Gs98AyvQXx6HSR1Qft`
- Copytrade **ce wallet seul** (pas le ring entier → sinon N buys par lancement).

## Config
- **Entrée** : mirror des buys, viser block 0 (fill réaliste = close de bougie).
- **TP étagé** : 50% de la position à **+50%**, 50% à **+150%**.
- **Position** : **$50 max** (règle perso, non négociable).
- **Variante à tester** : TSL pour capter les gros runners (médiane ATH +121%, max +1837%).

## Base de la config
- Taux d'atteinte réels (échantillon 60) : +50% → 95%, +150% → 42%.
- EV/trade modélisée étagé 50/150 : ~+57% (net frais, sous hypothèses).

## Risques identifiés
1. **Biais de survivant** — échantillon = top-ATH ; wallet complet 533/656 rug. Taux réels < modèle.
2. **Lmiss hypothétique** — pas de chemin de baisse. Non backtesté.
3. **Contention de landing** — placement élite en data, mais arriver block 0 en live sous congestion n'est pas garanti.

## Checklist d'activation (à cocher AVANT live)
- [ ] 48h de paper trading effectuées
- [ ] ≥20 lancements observés sur ≥72h
- [ ] Taux d'atteinte +50% réel mesuré (pas l'échantillon top-ATH)
- [ ] EV réelle positive après frais sur données paper
- [ ] Validation humaine (Akeno)

## Journal des versions
| Version | Date | Changement |
|---|---|---|
| v1 | 2026-08-15 | Création — config étagée 50/150, statut PAPER |
