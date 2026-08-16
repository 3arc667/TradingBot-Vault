---
protocole: test-TSL-40k
date: 2026-08-16
wallet_cible: E7T1Vs (copytrade)
statut: à exécuter (mesure — aucun tracker modifié)
lie_a: [05-ANALYSES/2026-08-16_analyse-fill-E7T1Vs.md, erreur-006]
---

# Protocole test — Trailing stop activation 40k MC vs TP fixe (E7T1Vs)

## Objectif
Mesurer si un trailing stop **armé à 40k MC** capte plus que le TP fixe actuel (+33/35% + sortie MC 46,5–49,5k), et **quel % de drawdown** tient réellement sur des rugs bloc-0 rapides. Décider TSL vs TP fixe sur données, pas au feeling.

## Garde-fous (non négociables)
1. **Mesure d'abord.** Aucun changement de tracker sans validation Akeno.
2. **SL dur obligatoire sous 40k.** Un trail armé à 40k ne protège RIEN en dessous (pré-migration, là où partent la plupart des rugs). ⚠️ w01 (le seul wallet encore armé) n'a AUCUN SL → à corriger avant toute chose.
3. **n ≥ 20 closes sur ≥ 72h** avant toute conclusion (erreur-003).
4. Pic lu sur bougies **depuis l'entrée réelle**, jamais l'ATH bloc-0 gonflé.

## Contexte config actuelle (source trackers 2026-08-16)
- Seul acheteur E7T1Vs : **w01 (8Kh2)** — TP +35%, sortie MC 46 500, **SL OFF**, délai 1,5s, buy 0.4.
- w04 (B37U) : autoBuy coupé (3 pertes d'affilée), garde SL −75 + MC 49,5/55,5k en sortie.
- Graduation ~35k → **40k = tout juste post-migration**. Fenêtre trail utile = 40k → sortie MC (~46,5–49,5k) = **mince** tant que la sortie MC dure reste.

## Données à logger — prochains ≥20 closes E7T1Vs
| Token | Entrée (MC + %) | Pic MC | Pic % (base copytrade) | 40k touché ? | Rug avant 40k ? | Retrace pic→fill réel % | Temps pic→collapse (s) | Sortie réelle (raison + %) |
|-------|-----------------|--------|------------------------|--------------|-----------------|-------------------------|------------------------|----------------------------|
| | | | | | | | | |

## Métriques à calculer (après n≥20)
1. **Taux d'activation** : % tokens qui atteignent 40k MC. Faible → trail 40k inutile, il ne s'arme jamais.
2. **Rug-avant-40k** : % → mesure la dépendance au SL dur (le trail ne couvre pas cette zone).
3. **Retrace médian pic→fill** (parmi activés) = le drawdown qu'on mange VRAIMENT. À comparer aux candidats de drawdown trail (20 / 30 / 40%).
4. **Simulé** (honnête, optimiste sur le fill) : gain réalisé TP fixe +35 vs trail@40k pour chaque drawdown {20,30,40}. Marque l'écart.
5. **Vitesse pic→collapse** : si médiane trop basse (rug en quelques s), un trail ne se remplit pas au niveau visé → le fill prime sur le seuil.

## Règle de décision
Adopter TSL@40k **seulement si** : taux d'activation élevé **ET** retrace tolérable **ET** on relâche la sortie MC dure (sinon le trail ne bosse que sur 40k→~49,5k = marginal) **ET** SL dur posé sous 40k.
Sinon → rester TP fixe atteignable + SL dur. Le seuil 40k n'est pas la variable décisive ; le **fill** l'est.

## Ce que ce protocole NE fait PAS
- Ne conclut pas sur petit échantillon (n<20).
- Ne touche aucun tracker (validation Akeno requise pour tout changement).
- Ne traite pas la priorité : **poser un SL sur w01 passe avant l'optimisation TSL.**
