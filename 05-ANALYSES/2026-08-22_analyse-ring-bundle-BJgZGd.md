---
date: 2026-08-22
type: analyse
tags: [ring, coffre, distribution-industrielle, bundle, intrackable, method2]
verdict: RING WASH/BUNDLE INDUSTRIEL — INTRACKABLE (blindage) ; seul actionnable = 8tfUh (copy)
statut: 8tfUh à qualifier en copytrade
seed_token: Bn1Wy74owcLz85BAmb5VVHh22Rf7BDuSf9JJKdvypump
---

# Analyse — Ring de wash/bundle industriel (coffre BJgZGd)

## Point de départ
Remontée depuis un token rug (Bn1Wy…pump) et un top-trader tracké : **8tfUh**
(8tfUhLteNKgF9T74fqd43DaXzFSWXJJFZA3jHDw5TeZD).
Son bénéf (10 SOL) descend : 8tfUh -> 6WrPVUtPEADqY1rcdWjmwkwC5jPc6zoXnjgnKdQF3dA7
-> Z3sJhNwMEr7SNDWvHVGTKfzu5423J8THw1PYYpVwy6H (agrège ~885 SOL) -> **BJgZGd**.

## Structure du ring (3 étages, tous jetables)
1. **Coffre — BJgZGd** (BJgZGdZXunPyn4PGJTNcRHSAQqDzBhV74JiHJDfHmWrT)
   - 0 token créé. Reçoit de 18+ sources (954 / 515 / 200 SOL…). Pure trésorerie.
   - Pousse vers **63 wallets** par paires répétées ~750 + ~200/250 SOL (plusieurs "hub").
   - Jumeau coffre : 4kwMyUNQVYkKrUU9Zatf8cQsWbBy2tvGgtX4YWQX6gQb (funded 10 SOL pile pareil).
2. **Distributeur — 8txZUG** (8txZUGSkBdpDhMz4iDvCy6TySFgJSmpzeQZp1E8r6MLq)
   - Funded par BJgZGd il y a ~2h (reçu 800 SOL).
   - En **1h20** : 1000 CREATE ACCOUNT -> **1000 wallets frais uniques, 2 543 SOL distribués.**
     785/1000 reçoivent **1 à 5 SOL** (taille de launch, pas du rent).
3. **Feuilles — 1000 wallets frais**
   - Testés (AcFn19…, 8txZUG lui-même) : **token_count = 0. Aucune création de token.**
   - => couche de **bundle/makers** (achètent le même token pour simuler la demande)
     ou dispatch. **Pas des launchers.**

## Verdict
- **Rien à sniper** : les feuilles ne créent rien (Method 1 impossible).
- **Rien à copier proprement** : distributeurs neufs qui tournent (8txZUG a 2h, sera remplacé),
  feuilles à usage unique. Chaque étage est jetable **par design = blindage anti-tracking.**
- Confirme erreur-002 à l'échelle industrielle : coffre/distributeur/feuille = jamais la cible.

## Seul maillon actionnable
- **8tfUh** — le top-trader du départ. Vrai historique de trade, bénéf prouvé (a alimenté
  une trésorerie 885+). Candidat **copytrade Method 2** (qualifier sur géométrie d'entrée,
  pas sur les ventes). => à qualifier.

## Prochaines actions
- [ ] Qualifier 8tfUh en copytrade (Block 0 share, cadence, entry median)
- [ ] Si une CA "achetée en meute" par les feuilles est fournie -> confirmer bundle en 1 check
- [ ] Ne PAS armer de tracker sur BJgZGd / 8txZUG / feuilles (intrackable)
