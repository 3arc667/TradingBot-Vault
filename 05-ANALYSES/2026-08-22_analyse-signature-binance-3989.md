---
date: 2026-08-22
type: analyse
tags: [method1, signature-cex, binance, tracker-candidat, paper-requis]
verdict: PAS un tracker propre — 3.989 = montant standard du wallet (92,7% des sorties, 881 destinataires/2mois). Usine à launches mais ~50% rug (profil AoGef). Filtre anti-rug + PAPER requis.
tracker_cex: 5tzFkiKscXHK5ZXCGbXZxdw7gTjjD1mBwuoFbhUvuAi9
signature_sol: 3.989 (plage 3.9889–3.9891)
seed_token: Ej389zc1uotqSbBdf35eS3mDWGsVQNwjmPNMpna4pump
---

# Analyse — Signature Binance 5tzFki / 3.989 (Method 1)

## Origine
Token POSSWACK (Ej389zc…pump) signalé par Akeno comme financé par "Binance 2"
via une plage déjà trackée. Créateur résolu : 8RRuymrMNr1ogCKPPXT8DkyqHb7AaV4c7F5Wwe6XAjDi.

## Signature — CONFIRMÉE
- Funder = **Binance, hot wallet 5tzFkiKscXHK5ZXCGbXZxdw7gTjjD1mBwuoFbhUvuAi9** ("Binance 2").
- Montant exact **3.989 SOL** → plage hair-thin **3.9889 – 3.9891**.
- Balayage profond (40 pages / 8000 sorties) : **9 autres wallets** reçoivent exactement 3.989
  (+ le créateur = 10), sur ~32h (~1 toutes les 3h). Non épuisé → probablement plus.
- ⚠️ Le scoring rapide plafonne à 4 pages et renvoie 0 match — **artefact d'outil**.
  Le balayage profond fait foi : signature réelle.

## Perf (partielle — 2 launches vérifiés, 2 winners)
- POSSWACK (créateur 8RRuym) : 1ère bougie ~8,9k → pic ~43k MC (Method1 +547%). WIN.
- 6qkP5… (plus ancien wallet 3.989) : throwaway frais, 1 token (BUTT) → **GRADUÉ, pas dumpé.**
- => 2/2 gagnants, mais n=2. Ne PAS figer le TP sur ça (survivor-luck possible).

## ⚠️ CORRECTION (2026-08-22, CSV complet 5tzFki)
- **3.989 n'est PAS une empreinte rare : c'est 92,7% de tout ce que 5tzFki envoie.**
  881 destinataires uniques sur ~2 mois (25 juin → 22 août), ~1 toutes les 90 min.
- Le "9 wallets" de l'outil = fenêtre de scan étroite. Réalité = usine à launches à débit élevé.
- **Échantillon réparti (8 wallets / 10 tokens) : ~50% DUMP.**
  - Rugs : Mogcoon, PippinDuck (~1h), DuckCoon, Bibo (~6 min), Glusy. 
  - Runners : POSSWACK (43k), BUTT (grad), Bip (grad). SCATS vivant.
- => **Profil AoGef (pile ou face, gros winners + instant-rugs).** Le "2/2 winners" initial = survivor bias.
- **Snipe à plat = NON.** Seule voie = filtre anti-instant-rug (skip dump bloc 0-3, entrée retardée, SL floor) validé en PAPER. Penchant : sceptique.

## Tracker (structure prête, TP à confirmer)
- **Tracker = l'adresse Binance 5tzFki** (jamais les enfants).
- Plage **3.9889 – 3.9891**, **freshWalletOnly + keepAddress + removeIfNoLaunch**.
- Entrée ≈ **75% de la première bougie**. TP = à fixer sur sample complet.

## Prochaines actions
- [ ] Compléter le sample : scorer les ~8 autres wallets 3.989 (ou CSV Solscan des sorties 5tzFki) → viser ≥20 launches.
- [ ] Fixer TP + vrai taux de +100% sur le sample complet.
- [ ] **PAPER 48h obligatoire** + validation Akeno avant live. Rien d'armé pour l'instant.
