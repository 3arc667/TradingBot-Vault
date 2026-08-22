---
date: 2026-08-22
type: analyse
tags: [dev-usine, method1, buy-the-dip, floor]
devs:
  - AoGefnxF5CbZvbd2cvxv4Ex1E5j86dqEjehazRuMcMFe
  - gVDXhoGbePACvSqN7CZBtQXFW9eyJwsgudPEwSydAkx
verdict: auto-snipe systematique REJETE / buy-the-dip discretionnaire A TESTER
statut: paper-trading requis
---

# Analyse — Deux devs "usine" PumpFun

## Contexte
Deux serial deployers repérés. ATH récurrents ~10k MC, gros runs occasionnels,
mais ouverture chaotique : dev vend, gros dump, remontée aléatoire.
Idée testée : combiner avec du buy-the-dip.

## Dev 1 — AoGef (AoGefnxF5CbZvbd2cvxv4Ex1E5j86dqEjehazRuMcMFe)
- 387 tokens créés. Vraie usine.
- **Funding sale** : premiere mise via wallet mère 0.5 SOL, ancienne, puis 50+ sources
  mélangées. Recycle en interne. Pas de signature exchange réutilisable.
- Chaîne de cash-out identifiée : dev -> AX5UZcKJoGFgRB3eaZADgkZ4KMfh8H8gDYhsEQohSTFY
  (~650 SOL) + EnagYpTbP9WeRFzWdNGqDsrGDLyLneBS4Ghqw8WcNhu5 (~832 SOL)
  -> hotwallet Bybit iGdFcQoyR2MwbXMHQskhmNsqddZ6rinsipHc4TNSdwu (~563 SOL cyclés).
  Dépôts en montants signature X.99959.
- **Verdict tracker : NON.** Funding intraçable, AX5UZ = nœud de sortie (bon à
  cartographier, pas trackable). Historiquement "pas ouf" à sniper — confirmé par le funding sale.

## Dev 2 — gVDX (gVDXhoGbePACvSqN7CZBtQXFW9eyJwsgudPEwSydAkx)
- 272 tokens, 116 sur 30j. ~31% gradúent, ~78% survivent le premier move.
- Funded par un exchange, proprement (4.885396 SOL).
  MAIS ce montant exact ne se répète sur aucun autre wallet -> **pas de signature
  réutilisable, exchange non trackable.** Seul le wallet dev est trackable.

### Échantillon Method 1 (entrée ~75% première bougie, TP +100%, SL floor)
- Floor constant ~2 653 MC. Entrée type ~6 500 MC.
- 12 tokens lus (échantillon THIN, 25.5h de couverture) : 4 W / 8 L = **33% WR**
- **Gain moyen net : −7.02%** (chaque perdant ~−60% jusqu'au floor)
- Gagnants : +121%, +277%, +503%, +812% (peaks 22k / 44k / 70k MC)

### Lecture
- Le potentiel est réel (grosse queue). Deux fuites tuent l'edge :
  1. TP +100% fixe -> coupe les +500/+800% à +100%
  2. Entrée trop haute (~6.5k vs floor 2.65k) -> −60% plein sur chaque raté
- Auto-snipe systématique à plat = **négatif, rejeté.**

## Conclusion / stratégie à tester
- **Buy-the-dip discrétionnaire près du floor + trailing sur runners** (pas TP fixe).
  Justification : floor défini + net, downside minuscule à l'entrée basse,
  runners 4x–25x, queue épaisse. Uniquement APRÈS que le dev ait vendu 100% (vrai floor posé).
- Non automatisable proprement -> discrétionnaire.
- **Paper trading 48h obligatoire avant réel** (règle perso).
- Échantillon à élargir (>20 tokens / >72h) pour figer les stats avant toute mise réelle.

## Prochaines actions
- [ ] Paper trade buy-the-dip gVDX, entrée proche floor, trailing stop
- [ ] Élargir échantillon gVDX (>20 launches)
- [ ] Continuer la liste de wallets trackés (autres candidats en attente)
