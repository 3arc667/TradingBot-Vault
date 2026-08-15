---
strategie: copytrade-E7T1Vs
version: v1
date_creation: 2026-08-15
wallet_cible: E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH
ring_reference: true
methode: copytrade (Method 2)
statut: 🟡 PAPER — validation à finaliser
paper_start: null
paper_end: null
validation_humaine: en attente
---

# Stratégie copytrade — E7T1Vs v1 (référence du ring)

> 🟡 **PAPER / validation à finaliser.** ⚠️ Ce wallet a été activé en live avant la fin des 48h paper (écart C1). À régulariser : soit compléter le protocole, soit documenter la dérogation.

## Cible
- Wallet : `E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH`
- **Référence unique du ring** (jumeau BxLm = backup, ne pas activer les deux → sinon 2 buys/lancement).

## Géométrie d'entrée (validée)
- Block-0 sur **99,7%** des entrées (652/654), médiane +0. Élite.
- Financé Binance Hot Wallet 2. 656 tokens, 62j.

## Config
- Entrée : mirror des buys.
- **Variante à tester (insight Akeno)** : **délai de 2s** avant entrée → skip la course block-0, contourne en partie le risque de landing.
- TP : à caler sur backtest bougie / paper (candidat étagé type 50/150 comme BxLm — même ring, distribution similaire).
- Position : **$50 max** (règle perso).

## Données de support
- Desk : block-0 99,7%, win réalisé 86%.
- Log manuel Akeno (2026-08-13) : 8 TP / 9 → direction confirmée. Magnitudes manuelles non fiables (erreur-003) → mesure = desk.

## Blocage de validation restant
- **Taux de fill TP réel non mesuré** (le seul blocker de fond depuis la validation copy wallet 1).
- Biais de survivant sur l'échantillon ATH (plafond, pas réalité).

## Checklist d'activation (AVANT live propre)
- [ ] Régulariser l'écart C1 (paper complété OU dérogation documentée)
- [ ] 48h paper trading
- [ ] ≥20 lancements observés sur ≥72h
- [ ] Taux de fill TP réel mesuré
- [ ] Variante délai 2s testée vs entrée immédiate
- [ ] Validation humaine (Akeno)

## Journal des versions
| Version | Date | Changement |
|---|---|---|
| v1 | 2026-08-15 | Création — référence du ring, note délai 2s, flag C1, statut PAPER |
