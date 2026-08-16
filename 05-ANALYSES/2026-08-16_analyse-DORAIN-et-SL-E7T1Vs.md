---
date: 2026-08-16
type: analyse
tokens: [DORAIN]
wallet_lie: E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH
source: desk Fproject
---

# Analyse 2026-08-16 — $DORAIN + justification SL E7T1Vs

## $DORAIN — non trackable en l'état
- CA : `D34f6e16ejHgSNCsRB4hBE9D5UEVTXCpNkNWwuB1pump`
- Symbole : DORAIN — MC ~$303 au check.
- **Créateur non résolu** par le desk → funder inconnu, 0 lancement antérieur, aucune signature CEX+montant.
- Verdict desk : `unknown`. À traiter comme **non-safe par défaut**, pas comme rugger connu.

### Décision
- **Ne pas tracker.** C'est un token, pas une adresse de ring. La stratégie suit le WALLET (E7T1Vs), pas les tokens à sec.
- Intéressant seulement si E7T1Vs le snipe → dans ce cas il apparaît dans les buys du tracker. Sinon, rien à en tirer.
- Rappel doctrine : le tracker = le wallet du ring (constante), jamais le dev/token jetable.

## Justification du SL −75 posé sur E7T1Vs (w04)
Données du run 2026-08-16 (voir journal-PnL) :
- $Tonguuue : **−100%** sur w04. Sans SL, plein tarif encaissé.
- $FOMOANSEM : **−12%** sur w04, sortie molle (coupe inactivité, pas stop).
- E7T1Vs n'avait **aucun SL** en v1 → exposition non bornée sur les entrées qui tournent mal.

### Lecture honnête
- Un SL −75 **n'aurait pas sauvé $Tonguuue** (rug trop rapide, saut direct sous le floor).
- Mais il **borne tous les dumps plus lents** et rend la collecte de données propre (pas de −100 qui pollue l'échantillon).
- Décision : SL −75 posé le 2026-08-16. Statut = collecte live bornée, réf unique.

## Piège évité
- Close manuelle Akeno sur $FOMOANSEM (+24% vs −12% auto) : **ne PAS** en conclure "main > auto".
  Échantillon = 1 token. C'est erreur-003 (petit échantillon pris pour mesure). Noté comme couleur uniquement.
- Le vrai argument de la donnée n'est pas "main vs auto" mais "il faut un SL". C'est ce qui a été acté.
