---
erreur: 006
date_detection: 2026-08-16
gravite: CRITIQUE
lie_a: C1
statut: régularisé (dérogation assumée)
wallets: [E7T1Vs w04, BxLm w01]
---

# Erreur 006 — Live sous label PAPER + double-buy sur le ring

## Ce qui s'est passé
En début de session, la fiche stratégie E7T1Vs affichait **statut PAPER / validation à finir**.
Le desk montrait la réalité inverse : **deux copytrades armés en live** (achat + vente auto), dernier fill 11 min avant :
- E7T1Vs (wallet 04) — buy 0.4 SOL
- BxLm (wallet 01) — buy 0.5 SOL

Deux problèmes cumulés :
1. **C1 en direct** : config live alors que la doc disait paper. Le seul blocker de fond (taux de fill TP) n'avait jamais été mesuré.
2. **Double-buy** : les deux réfs du ring achetaient en parallèle → 2 buys sur chaque token, taille et contention doublées. La v1 disait explicitement "une seule référence".

## Pourquoi c'est arrivé
- Pas de mémoire persistante entre sessions + fiche stratégie non synchronisée avec l'état réel du desk.
- Absence de vrai mode paper sur le desk : illusion qu'on "faisait du paper" alors que le seul état non-achat est l'observation.

## Correction appliquée (2026-08-16)
- **BxLm désarmé** (copy + achat + vente auto OFF) → fin du double-buy.
- **E7T1Vs gardé seul armé** (réf unique) + **SL −75 posé** pour borner la collecte.
- Statut fiche corrigé : PAPER (fictif) → LIVE borné assumé (v2), dérogation validée par Akeno.
- C1 coché dans erreurs-recurrentes.md.

## Règle à tenir
- **Toujours lire l'état réel du desk (trackers armés) avant de croire un statut de fiche.** La fiche peut mentir, le desk non.
- Ne jamais laisser 2 réfs d'un même ring armées en parallèle.
- "Paper" sur ce desk = observation (pas d'achat, pas de fill). Si on veut du fill réel, c'est du live borné assumé — pas un faux paper.
