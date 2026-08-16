---
analyse: fill-E7T1Vs
date: 2026-08-16
wallet: E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH
methode: copytrade (Method 2)
fenetre: ~72h
n_tokens: 46
base_mesure: ath_pct_copytrade (entrée follower réaliste, PAS ath bloc-0 du ring)
source: desk Fproject (rapport wallet profond)
---

# Analyse fill / distribution — E7T1Vs (72h, n=46)

## Objet
Mesurer la distribution des pics **atteignables depuis une entrée copytrade réaliste** (pas l'ATH bloc-0 du ring, qui est gonflé). Base du calage TP + du taux de fill.

## Profil wallet (contexte)
- 666 tokens, 63j, bloc-0 sur **99,7%** des entrées. Financé Binance HW2 (0,099 SOL).
- copytrade_score 75, rugger_score 83. Ring confirmé (24 wallets co-financés).
- Distribution de sortie du wallet lui-même (base bloc-0, tout historique) : rugged ~399, loss ~153, breakeven→2x ~75, 2–5x ~102, 5x+ ~9. **Le bucket dominant = rug.**

## Distribution des pics atteignables — 72h, base copytrade (n=46)
| Seuil | % tokens qui l'atteignent |
|-------|---------------------------|
| +30%  | 89% (41/46) |
| +50%  | 80% (37/46) |
| +70%  | 65% (30/46) |
| +100% | 52% (24/46) |
| +120% | 43% (20/46) |
| pic médian | ≈ +102% |

## Lecture
- **Correction d'un diagnostic antérieur faux** : j'avais dit « +120 hors de portée, max +69 » sur la base de 6 closes réalisés (16/08) = biais petit échantillon (erreur-003). La vraie mesure 72h dit **+120 atteint 43%**.
- **MAIS atteignable ≠ rempli.** Les closes réalisés du desk (16/08 : +56/+59/+69) sont très en dessous du pic atteignable. Le prix touche le niveau, le desk n'y **vend** pas.
- Le gap = **timing d'exit sur rug bloc-0** (délai ~1,5s → la tranche haute redescend avant d'être vendue). C'est LE taux de fill réel, toujours non mesuré directement.
- ⚠️ L'ATH atteignable est un **plafond** (biais de survivant), jamais un prix garanti vendable.

## Conséquence pour le TP
- Le problème du 50/120 n'est PAS que +120 est hors de portée (il ne l'est pas).
- Le problème = la 2e tranche ne se **remplit** pas au niveau visé sur ces rugs rapides → elle ride vers SL −75 / rug.
- Levier réel : soit baisser la 2e tranche là où l'exit remplit vraiment (à mesurer), soit tranche unique atteignable, soit corriger le mécanisme/délai d'exit.

## À faire (mesure du fill vrai)
1. Logger, sur les ≥20 prochains closes live : pic atteignable vs % réellement encaissé.
2. Gap moyen = perte de fill. C'est ça la donnée manquante depuis la validation du wallet.
3. Aucune conclusion config avant n≥20 (erreur-003).

## Décision en attente (Akeno)
- a) Tranche unique atteignable (~+40/+50, fill fiable)
- b) Garder étagé mais 2e tranche plus basse (~+80) où le fill est plausible
- c) Halte E7T1Vs le temps de mesurer le fill
