---
erreur: 006
titre: TP étagé non backtesté déployé live sur E7T1Vs — diagnostic initial faux (biais 6 tokens), corrigé
gravite: majeure
date_detection: 2026-08-16
date_correction: 2026-08-16
lie_a: [erreur-001, erreur-003, erreur-005, C1]
wallet: E7T1Vs (w04)
statut: ouverte — attente arbitrage Akeno
---

# Erreur-006 — TP étagé 50/120 poussé en live sans validation sur E7T1Vs

## Ce qui s'est passé
- Config live sur E7T1Vs (w04) : TP étagé **50% @ +50% / 100% @ +120%**, SL −75.
- Ce +50/+120 n'a **jamais été backtesté ni mesuré** au moment du déploiement. Candidat recopié de BxLm, poussé en live (rattaché à l'écart C1).

## ⚠️ CORRECTION 2026-08-16 (même session — j'ai reproduit erreur-003)
- **Diagnostic initial FAUX.** J'avais écrit : « 2e tranche +120 hors de portée du ring, meilleur token = +69 ». C'était tiré du run de **6 tokens** du 16/08 (closes réalisés du desk) — exactement le biais petit échantillon (erreur-003) que je venais de dénoncer.
- **Mesure réelle 72h (n=46, base copytrade = entrée follower réaliste, pas ATH bloc-0) :**
  - +30% atteint : **89%** des tokens (41/46)
  - +50% atteint : **80%** (37/46)
  - +100% atteint : **52%** (24/46)
  - +120% atteint : **43%** (20/46)
  - Pic médian atteignable ≈ **+102%**
- Donc **+120 est atteint ~44% du temps**, pas « jamais ». Mon plafond +69 était faux.

## Le vrai défaut (reformulé)
- **Atteignable ≠ rempli.** Le prix touche +120 dans 44% des cas, mais le desk n'y *vend* pas : closes réalisés 16/08 = +56/+59/+69, très en dessous du pic atteignable.
- Cause probable : rugs bloc-0 rapides + délai ~1,5s → la 2e tranche ne se remplit pas au pic, elle redescend vers SL −75 / rug.
- Le blocker de fond reste donc le **taux de fill réel** (vendre vraiment au niveau), pas la hauteur de la cible. C'est ce que la stratégie flaggait déjà comme non mesuré.
- ⚠️ Rappel : l'ATH atteignable est un **plafond** (biais de survivant), pas un prix vendable. Seuls les closes réalisés live donnent le fill vrai — échantillon encore petit.

## Correction / next
- Ne PAS conclure config sur les closes réalisés tant que n < ~20 (erreur-003).
- Mesurer le fill réel sur les prochains closes live vs pic atteignable → mesure le gap timing.
- Décision TP (tranche unique atteignable vs garder étagé plus bas type +80 vs halte) = arbitrage Akeno, pas de lock unilatéral (erreur-001).

## Règle retenue
Un pic atteignable élevé ne vaut pas fill. Sur snipe bloc-0 de rugger, la cible haute d'une tranche ne sert que si l'exit la remplit — sinon c'est une tranche exposée au rug. Mesurer le fill, ne pas déduire de l'ATH.
