---
id: erreur-005
date: 2026-08-15
type: méthodologie / outil
gravité: moyenne
statut: documentée
---

# Erreur-005 — Backtest bougie inutilisable pour mesurer les fills TP (couverture d'entrée)

## Contexte
Tentative de backtest bougie sur la config copytrade ring (50/150) pour mesurer le taux de fill TP réel avant la fin du paper.

## Le problème
L'outil bougie ne prend **pas** de paramètre de date de départ : il rend les **N dernières bougies par nombre**. Sur des tokens qui vivent 12h+, une fenêtre de 300–500 bougies tombe dans **la descente vers le floor**, jamais dans le pump initial.

Vérifié sur 2 tokens :
- Gw7U : bougie la plus ancienne rendue ≈ **+48 min** après l'entrée du wallet.
- 5p2a : bougie la plus ancienne rendue ≈ **+24 min** après l'entrée.

Or les fills TP (+50/+150) se jouent à la **montée juste après l'entrée** — précisément la zone hors de portée. Le peak est déjà connu (ATH copytrade desk) ; le backtest devait apporter le *chemin* (TP touché avant le dump ?), et c'est ce qu'on ne peut pas voir.

## Règle
- **Ne pas relancer ce backtest bougie à l'aveugle** pour mesurer des fills TP sur des tokens longue durée : l'outil ne remonte pas jusqu'à l'entrée.
- La mesure du taux de fill TP passe par le **paper trading** (capte les entrées en direct), pas par l'historique bougie.
- Ne jamais fabriquer un chiffre de fill pour combler le trou (rappel : never invent OHLC / ATH).

## Lien
- Renforce le gate vault : validation via paper, pas via backtest.
