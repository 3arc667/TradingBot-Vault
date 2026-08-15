# 🧪 TEST COMPLET — Vérification lecture/écriture MCP

> Fichier de test généré pour valider la chaîne complète MCP Filesystem.
> Zone temporaire — à supprimer après vérification.

## Contexte
- **Date** : 2026-08-15
- **Objectif** : confirmer que Claude lit le vault ET écrit sur disque
- **Portée** : opération vault-interne uniquement (aucun trade, aucune exécution)

## Checklist test

| # | Action | Cible | Statut |
|---|--------|-------|--------|
| 1 | Lecture vault | PROMPT-SYSTEM / SCHEMAS-RUGGERS / erreurs-recurrentes / journal-PnL | ✅ OK |
| 2 | Écriture fichier test | 99-TEMP/test-complet.md | ✅ OK (ce fichier) |
| 3 | Update journal-PnL | 07-PERFORMANCE/journal-PnL.md | → en cours |
| 4 | Relecture / confirmation | tous | → à valider |

## Rappel règles perso (contrôle de cohérence)
- Position max : 50$ / trade
- Stop journalier : -200$ → arrêt
- Pas de martingale
- Paper trading 48h avant live sur nouvelle stratégie
- Validation humaine obligatoire avant tout trade

---
*Source : MCP Filesystem — écriture directe disque.*
