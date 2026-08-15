# 📚 README — TradingBot Vault

## 🎯 Qu'est-ce que ce vault ?
C'est le cerveau de mon bot de trading. Claude écrit directement ici via MCP Filesystem.

## 📁 Structure

| Dossier | Contenu | Qui écrit ? |
|---------|---------|-------------|
| `00-SYSTEM` | Règles, prompts, commandes | Moi (manuel) |
| `01-CONFIG` | Configurations bot/wallet | Moi (manuel) |
| `02-RUGGERS` | Types de ruggers identifiés | Claude (auto) |
| `03-STRATEGIES` | Stratégies validées par rugger | Claude (auto) |
| `04-TRADES` | Historique de tous les trades | Claude (auto) |
| `05-ANALYSES` | Analyses détaillées | Claude (auto) |
| `06-ERREURS` | Erreurs et corrections | Claude (auto) |
| `07-PERFORMANCE` | PnL, winrate, métriques | Claude (auto) |
| `99-TEMP` | Brouillons et tests | Claude (auto) |

## 🚀 Workflow
1. Je trade avec Fproject
2. Claude analyse et écrit dans le vault (auto)
3. Je vérifie et sync sur GitHub (manuel)