---
strategie: copytrade-E7T1Vs
version: v3
date_creation: 2026-08-16
wallet_cible: E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH
wallet_execution: 8Kh29F7i18ui3WtHy8GngCEXcyyBTxTpCd4JTts1ksCt (wallet 01 — seul armé au 16/08 soir)
ring_reference: true
methode: copytrade (Method 2)
statut: 🟡 À MESURER — structure proposée, chiffres NON validés (hypothèse de départ)
remplace: strategie-copytrade-E7T1Vs-v2.md
validation_humaine: en attente (chiffres à figer après collecte)
lie_a: [05-ANALYSES/2026-08-16_analyse-fill-E7T1Vs.md, 05-ANALYSES/2026-08-16_protocole-test-TSL-40k.md, erreur-006, C1]
---

# Stratégie copytrade — E7T1Vs v3 (sortie en couches)

> 🟡 **Structure proposée, pas une config validée.** Les chiffres ci-dessous sont des
> **valeurs de départ** à resserrer sur données (protocole TSL). Les graver en dur
> sans mesure = erreur-001. Aucun tracker modifié par le desk.

## Pourquoi v3 remplace v2
- v2 décrivait une « config figée 50/120 + SL −75 sur w04 » — **fausse** vs trackers réels.
- v2 s'appuyait sur « +69 plafond » (6 tokens) — biais petit échantillon, corrigé (erreur-006).
- État réel corrigé ci-dessous.

## État live réel au 16/08 (soir) — source trackers
- **Seul acheteur E7T1Vs = wallet 01 (8Kh2).** autoBuy ON. TP +35% / sortie MC 46 500 / **SL OFF** / délai 1,5s / buy 0.4.
- Wallet 04 (B37U) : autoBuy **coupé** (3 pertes d'affilée). Garde SL −75 + MC 49,5/55,5k, ne rachète plus.
- Double-buy **fermé** (un seul acheteur). ⚠️ mais le wallet resté armé (w01) est **sans stop** → priorité #1 = poser le SL.

## Ce que dit la donnée (fill 72h, n=46 — base copytrade réelle)
- +30 atteint 89% · +50 80% · +100 52% · +120 43% · **pic médian ≈ +102%**.
- Distribution = **gros paquet de verts médians qui plafonnent bas + queue de runners**.
- ⚠️ Atteignable ≠ rempli : le pic est un plafond, le fill réel (surtout sur rug bloc-0 rapide) est plus bas. C'est LE trou à mesurer.

## Logique de la sortie en couches (le "quoi mettre")
Un seul outil laisse toujours de l'argent :
- **TP fixe seul** = garantit la prise mais plafonne (rate la queue).
- **TSL seul** = laisse courir mais rend le drawdown ET ne banke pas le token qui top bas.
→ La distribution a les deux profils → on empile les deux.

## Config proposée (hypothèse de départ — À MESURER, pas validée)
| Couche | Rôle | Valeur de départ | À caler sur |
|---|---|---|---|
| **Tranche fixe** | banker le médian | vendre ~**50% @ +40/+50%** | fill réel du niveau |
| **TSL (solde ~50%)** | capter la queue | activation **basse ~15–20k MC** (PAS 40k), drawdown **−20/−25%** | protocole TSL (retrace pic→fill) |
| **SL dur** | borne pré-40k | **−75%**, 100% position | garde |
| **No-activity** | filet | **300s** | garde |
| Buy / délai | — | 0.4 SOL / ~1,5s | — |
| Buy once / pertes max | — | ON / 3 | — |

### Note sur le seuil d'activation du TSL
- **40k = post-migration** : n'arme le trail que pour les gros runners → tout ce qui top sous 40k n'a plus de prise de profit (TP fixe retiré). D'où la **tranche fixe** qui couvre cette zone.
- Armer le trail **bas (15–20k)** couvre aussi le winner médian. Le protocole mesure le taux d'activation à chaque seuil → on tranche sur chiffres.
- **Drawdown −35% = trop large** pour des rugs bloc-0 (traverse avant le fill). Démarrer **−20/−25%**, resserrer/élargir sur données.

### Si on retire le cap MC dur
- Retirer la sortie MC (46,5–49,5k) = nécessaire pour laisser courir la queue.
- MAIS alors le TSL **doit** exister pour ne pas rider jusqu'au SL. Ne jamais retirer le cap MC sans trail armé en dessous.

## Priorités (ordre)
1. **Poser le SL −75 sur w01** (seul armé, actuellement nu). Avant tout le reste.
2. Décider tranche fixe + TSL (structure ci-dessus) — hypothèse de départ.
3. **Collecter ≥20 closes** (protocole TSL) : 40k touché ? retrace pic→fill ? vitesse collapse ?
4. Resserrer les chiffres sur données → figer en v4 « validée ».

## Checklist avant v4 "validée"
- [ ] SL posé sur w01
- [ ] Structure en couches en place (fixe + TSL + SL + no-activity)
- [ ] ≥20 closes loggés sur ≥72h (erreur-003)
- [ ] Taux d'activation par seuil MC mesuré
- [ ] Retrace médian pic→fill mesuré → drawdown TSL calé
- [ ] Revue Akeno → figer v4

## Journal des versions
| Version | Date | Changement |
|---|---|---|
| v1 | 2026-08-15 | Création — réf ring, statut PAPER |
| v2 | 2026-08-16 | Réf w04 + SL −75, statut LIVE borné (PÉRIMÉ — config figée fausse vs trackers) |
| v3 | 2026-08-16 | Corrige l'état réel (w01 seul armé sans SL) ; structure de sortie en couches (TP fixe + TSL bas + SL dur) posée en hypothèse à mesurer ; chiffres NON validés |
