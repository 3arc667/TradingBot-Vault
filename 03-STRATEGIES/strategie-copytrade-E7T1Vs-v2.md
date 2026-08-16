---
strategie: copytrade-E7T1Vs
version: v2
date_creation: 2026-08-16
wallet_cible: E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH
wallet_execution: B37UkzxL9PYudqVatPgCzF34UfH4AfkYH7ZjmcEjLBtF (wallet 04)
ring_reference: true
methode: copytrade (Method 2)
statut: 🟢 LIVE BORNÉ — collecte de données (dérogation C1 assumée)
paper_start: null
paper_end: null
validation_humaine: dérogation validée par Akeno 2026-08-16
remplace: strategie-copytrade-E7T1Vs-v1.md
---

# Stratégie copytrade — E7T1Vs v2 (référence unique du ring)

> 🟢 **LIVE borné, un seul wallet.** Décision Akeno 2026-08-16 : garder 1 wallet armé pour
> collecter de la donnée réelle plutôt que repasser en observation (le desk n'a pas de vrai
> mode paper — voir note ci-dessous). BxLm désarmé le même jour. SL −75 ajouté pour borner.

## Changements vs v1
- **Réf unique = E7T1Vs sur wallet 04** (B37U…LBtF). BxLm (wallet 01) DÉSARMÉ → fin du double-buy sur chaque token du ring.
- **SL −75% ajouté** (n'existait pas en v1). Justifié par la donnée : $Tonguuue −100% non borné, $FOMOANSEM −12% en sortie molle (voir 05-ANALYSES 2026-08-16).
- Statut passé de PAPER (fictif) à LIVE borné assumé.

## Cible
- Wallet suivi : `E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH` (réf du ring, block-0 99,7%).
- Wallet d'exécution : `B37UkzxL9PYudqVatPgCzF34UfH4AfkYH7ZjmcEjLBtF` (wallet 04).
- BxLm (`BxLmrDJaNr9hA35FBGASAhUK74Gs98AyvQXx6HSR1Qft`) = backup, DÉSARMÉ. Ne pas réarmer en parallèle (sinon 2 buys/lancement).

## Config live figée (2026-08-16)
| Champ | Valeur |
|---|---|
| Copy / achat auto / vente auto | ON / ON / ON |
| Buy | 0.4 SOL (~$30) |
| Délai | ~1,5s (delay 2 / snipeDelayMs 1500) |
| TP étagé | 50% de la position @ +50%, reste @ +120% |
| SL | −75% (100% de la position) |
| Sortie MC | 49 500 |
| Buy once | ON |
| Coupe inactivité | 5 min |
| Pertes conséc. max | 3 |
| Taille sous cap perso | oui ($30 < $50/$150) |

## Note honnête — "mesurer le fill TP"
Le desk n'a que deux états : armé (achète pour de vrai) ou observation (voit les signaux, n'achète pas).
**Pas de simulateur paper.** En observation, pas de position = pas de fill TP mesurable.
→ La validation Méthode 2 se fait sur la **géométrie d'entrée** (block-0, timing, cadence), conforme au smart-core.
→ Le taux de fill TP réel ne sortira que de fills réels = cette collecte live bornée.

## Ce que la donnée a déjà montré (run du 2026-08-15/16, 6 tokens)
- TP étagé E7T1Vs laisse courir : +69 / +59 / +56 (CATU / RM / Dockey) vs +34 / +22 / +31 pour BxLm flat.
- Quand ça marche, w04 encaisse plus. Quand ça rug, même sanction → d'où le SL.
- 1 close manuelle Akeno sur BxLm ($FOMOANSEM +24%) : notée comme couleur, PAS comme preuve main > auto (échantillon = 1, cf. erreur-003).

## Checklist collecte (avant de figer une v3 "validée")
- [x] Régulariser C1 (dérogation documentée)
- [x] Réf unique armée (E7T1Vs w04), backup coupé (BxLm)
- [x] SL posé pour borner les pertes
- [ ] ≥20 fills réels observés sur ≥72h
- [ ] Taux de fill TP réel mesuré (sur fills live)
- [ ] Comparaison délai 1,5s vs immédiat (optionnel, plus tard)
- [ ] Revue Akeno → décision v3 (garder / ajuster / couper)

## Journal des versions
| Version | Date | Changement |
|---|---|---|
| v1 | 2026-08-15 | Création — réf du ring, note délai 2s, flag C1, statut PAPER |
| v2 | 2026-08-16 | Réf unique w04, BxLm désarmé, SL −75 ajouté, statut LIVE borné (dérogation C1 assumée) |
