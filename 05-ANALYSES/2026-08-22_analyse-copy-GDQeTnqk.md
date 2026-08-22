---
date: 2026-08-22
type: analyse
tags: [copytrade, method2, scalper, candidat, paper-requis]
wallet: GDQeTnqkyeLyRSjWaeFY5HsxaWoQmmXFc1N6wyuuHiQD
verdict: CANDIDAT COPY SÉRIEUX mais FRAGILE — paper 48h obligatoire (mesurer le fill)
funding: Binance 10.199 SOL (sig 10.1989–10.1991)
---

# Analyse copy — GDQeTnqk (scalpeur HF)

## ⚠️ Correctif index
Le desk Fproject l'a renvoyé **dead/stale / n=0** → FAUX (trou d'index Terminal).
Export DeFi on-chain (Solscan) = wallet **très actif**. Toujours vérifier le CSV avant de
classer un wallet mort.

## Profil réel (export 1000 swaps, 9,5 j : 2026-08-12 → 08-22)
- 342 achats / 622 ventes sur **342 tokens** (≈1 achat/token, scale-out en plusieurs ventes).
- **Win rate aller-retour : 63,5%.**
- **0 sac gardé** — sort systématiquement (aucun baghold dans la fenêtre).
- Pertes capées ~−1 SOL ; meilleurs coups +1,8 / +2,9 / +3,0.
- Taille uniforme **~2 SOL** (médiane 2,0). **Net +54 SOL** sur la période.
- Cadence **~1,5 achat/h** (au-dessus de l'idéal copy ≤1/h).
- **Hold médian ~0 min — 100% des trades bouclés en <10 min** (scalp ultra-rapide).
- Funding : **Binance, 10.199 SOL**, signature 10.1989–10.1991 (propre).

## Verdict
- **Bon trader, discipliné.** Mais copy **FRAGILE** :
  - Gain **médian ~0,03 SOL** < coût d'un aller-retour (~0,044) → l'edge vit dans la **queue** (gros winners).
  - Scalp <10 min → un fill copié un cheveu derrière le sien efface la marge sur les petits trades.
- Copyable SEULEMENT si : coller à sa vitesse (Block 0), ne pas rater les gros, **monter la taille** (jamais couper les frais).

## Prochaine action
- [ ] **Paper trade 48h obligatoire** — mesurer MON fill réel vs le sien (c'est tout le jeu ici).
- [ ] Si le fill tient (petits trades ≥ break-even après frais) → copy live borné, une seule référence.
- [ ] Sinon → reject (frais > edge).
- 8tfUh écarté (n'a tradé que Bn1Wy = participant one-shot du ring, pas un scalpeur).
