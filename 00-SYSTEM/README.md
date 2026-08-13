# 📚 README — TradingBot Vault

## 🎯 Qu'est-ce que ce vault ?
C'est le cerveau de ton bot de trading. Tout ce que Claude apprend, découvre, ou corrige est écrit ici.

## 📁 Structure rapide

| Dossier | Contenu |
|---------|---------|
| `00-SYSTEM` | Règles, prompt système, glossaire |
| `01-CONFIG` | Configurations du bot et du wallet |
| `02-RUGGERS` | Base de données des types de ruggers |
| `03-STRATEGIES` | Stratégies par type de rugger |
| `04-TRADES` | Historique de tous les trades |
| `05-ANALYSES` | Analyses de marché et patterns |
| `06-ERREURS` | **LE PLUS IMPORTANT** — Erreurs et corrections |
| `07-PERFORMANCE` | PnL, winrate, métriques |
| `99-TEMP` | Brouillons (auto-purge) |

## 🚀 Comment utiliser ce vault avec Claude

1. **Avant chaque session** : Demande à Claude de relire `00-SYSTEM/PROMPT-SYSTEM.md`
2. **Pendant la session** : Claude écrit directement dans les dossiers
3. **Après chaque trade** : Vérifie que Claude a créé la fiche dans `04-TRADES/`
4. **En cas d'erreur** : Vérifie que Claude a créé `06-ERREURS/erreur-XXX.md`

## ⚠️ Règles d'or
- **Jamais de clés privées/API ici**
- **Toujours relire avant de trader**
- **Documenter chaque erreur**
