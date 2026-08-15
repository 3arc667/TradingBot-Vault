---
type: paper-trading
config: copytrade-ring-v1 (banc = BxLm)
statut: 🟢 PAPER EN COURS — aucun capital réel
start: 2026-08-15T22:15Z
end_cible: 2026-08-17T22:15Z (48h)
wallet_banc: BxLmrDJaNr9hA35FBGASAhUK74Gs98AyvQXx6HSR1Qft
ring_reference_live: E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH
validation_humaine_live: NON — requise à la sortie
---

# Paper trading — config ring (banc BxLm)

> 🟢 **PAPER EN COURS.** Simulation seule, zéro capital. BxLm sert de banc pour mesurer la config du ring sans ajouter d'exposition live (E7T1Vs tourne déjà). Aucun live BxLm.

## Fenêtre
- Début : **2026-08-15 22:15 UTC**
- Fin cible : **2026-08-17 22:15 UTC** (48h)
- Gate lancements : **≥20 sur ≥72h** (prolonger si <20 à 48h)

## Config testée
- Copytrade mirror des buys de BxLm.
- TP **étagé 50/150** (moitié +50%, moitié +150%).
- Position notionnelle **$50**.
- Variante en parallèle : **délai d'entrée 2s** (insight Akeno) vs entrée immédiate.

## Objectif de mesure
**Le taux de fill TP réel** — sur TOUS les lancements de la fenêtre, pas un échantillon choisi. C'est la mesure qui manque depuis la validation copy wallet 1.

## Prior fourni par Akeno (données manuelles, biais de sélection assumé)
- Log E7T1Vs : **13 TP / 14** (~93%).
- Log BxLm : **12 / 12** (100%).
- ⚠️ Échantillon choisi à la main (~35 MC), pas la population complète (majorité rug). ATH manuels ≈ moitié de l'ATH copytrade desk. → hypothèse encourageante, à confirmer sur tous les lancements.

## Critères de sortie → passage live (TOUS requis)
- [ ] ≥20 lancements observés / ≥72h
- [ ] Taux de fill TP réel mesuré (pas le prior manuel)
- [ ] EV nette positive après frais sur données paper
- [ ] Variante 2s tranchée vs immédiat
- [ ] Écart C1 (E7T1Vs live) régularisé
- [ ] **Validation humaine explicite (Akeno)**

## Journal paper
| Date | Lancements observés | TP fill réel | Note |
|---|---|---|---|
| 2026-08-15 | 0 (start) | — | compteur démarré, prior loggé |
