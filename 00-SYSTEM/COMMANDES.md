
# 📋 COMMANDES & PROMPTS — SnipeRugger AI


---

🚀 DÉBUT DE SESSION
---

SESSION TRADING — Démarrage

1. CHARGE LE CERVEAU FPROJECT :
   - fproject_brain({section:"voice"})
   - fproject_brain({section:"kernel"})
   - fproject_brain({section:"smart-core"})

2. RELIS MON VAULT via MCP Filesystem :
   - C:\TradingBot\00-SYSTEM\PROMPT-SYSTEM.md
   - C:\TradingBot\02-RUGGERS\SCHEMAS-RUGGERS.md
   - C:\TradingBot\06-ERREURS\erreurs-recurrentes.md
   - C:\TradingBot\07-PERFORMANCE\journal-PnL.md

3. RÉSUME-MOI :
   - Mon PnL actuel (journalier/cumulé)
   - Mes ruggers actifs et leurs configs
   - Mes erreurs à ne pas répéter
   - L'état du marché aujourd'hui (volatilité, opportunities)

4. QUE FAISONS-NOUS AUJOURD'HUI ?
   [Attends ma réponse : analyse token / trouver rugger / portfolio / setup tracker]
   --- 

## ⚡ RACCOURCI ANALYSE WALLET + SIMULATION

ANALYSE WALLET + SIMULATION

Adresse : [ADRESSE]

1. Deep dig Fproject (wallet + qualify + candles)
2. Config optimale (TP/SL/buy amount)
3. Simulation sur 20-30 derniers tokens
4. Verdict GO/NO GO
5. Écris tout dans le vault
---




🔍 ANALYSER UN TOKEN/DEV 
--- 

ANALYSE CE TOKEN/DEV

Adresse : [METS L'ADRESSE ICI]

1. Deep dig Fproject (cex_research ou qualify)
2. Type de rugger ?
3. Config proposée ?
4. GO ou NO GO ?

Garde les détails techniques pour l'archive.

---
🎯 TROUVER UN RUGGER
---

TROUVE-MOI UN RUGGER À SNIPE

1. Easy Snipe Fproject
2. Si trouvé : type, config, GO/NO GO
3. Si rien : pourquoi, quoi surveiller
   
   ---
💰 PORTFOLIO & SELL
---
ÉTAT DU PORTFOLIO

1. Portfolio overview Fproject
2. Positions ouvertes — lesquelles sell ?
3. PnL actuel
4. Stop atteint ?

---
   📝 ARCHIVER UNE ANALYSE (à la fin)

---

ARCHIVE CETTE ANALYSE


Génère tous les fichiers à copier dans mon vault :

1. Fiche analyse détaillée (05-ANALYSES/)
2. Màj SCHEMAS-RUGGERS si nouveau pattern
3. Màj correlations.md si corrélation trouvée
4. Stratégie si nouvelle/validée (03-STRATEGIES/)
5. Trade si exécuté (04-TRADES/)
6. Erreur si perte (06-ERREURS/)

Format : texte brut prêt à copier-coller avec chemins exacts.

   
---
❌ ARCHIVER UNE ERREUR
--
ARCHIVE CETTE ERREUR

Token : [ADRESSE]
Montant perdu : [$X]
Description : [QUE S'EST-IL PASSÉ]

Génère :
1. Fiche erreur-XXX.md complète
2. Màj erreurs-recurrentes.md
3. Correction proposée
4. Vérification à faire

Format : texte brut prêt à copier-coller.

---
📊 MÀJ PNL
--
MÀJ PNL

Date : [DATE]
Trades aujourd'hui : [X]
Gains : [$X]
Pertes : [$X]
PnL jour : [+$X / -$X]

Génère la ligne à ajouter dans journal-PnL.md

---

🔧 Push sur git hub
---
Ctrl + P → "Obsidian Git: Commit and push"

---
## 🔍 PROMPT ANALYSE WALLET + SIMULATION

SESSION TRADING — Analyse wallet + simulation

1. CHARGE LE CERVEAU FPROJECT (voice, kernel, smart-core)
2. RELIS MON VAULT via MCP Filesystem

3. ANALYSE CE WALLET EN PROFONDEUR :
   Adresse : [METS L'ADRESSE ICI]

   a) Historique d'achats complet (Fproject rugger_wallet)
   b) Entry blocks / placement / copytrade_score
   c) ATH % depuis entry (30-50 derniers tokens)
   d) Winrate, cadence, consistence
   e) Funding origin / CEX pattern si applicable
   f) Type de rugger associé (si c'est un dev)

4. QUALIFICATION :
   - Method 1 (snipe dev) ou Method 2 (copytrade) ?
   - Bible qualified ? Oui/Non + pourquoi
   - Sample size suffisant ? (≥20 tokens / ≥72h)

5. CONFIGURATION OPTIMALE :
   - TP calculé depuis ath_pct_copytrade (distribution, ≥5/30 bar)
   - SL : natural floor ou fixe ?
   - Buy amount : fee floor §9 + supply share
   - Snipe delay si nécessaire
   - Rugger Protection si CEX pattern
   - MinMC/MaxMC si copytrade

6. SIMULATION :
   - Sur les 20-30 derniers tokens du wallet
   - Applique la config proposée
   - Calcule : winrate, PnL total, ratio gain/perte
   - Compare avec d'autres TP possibles (+80%, +120%, etc.)
   - Quelle config maximise le total expected gain ?

7. ÉCRIS DANS LE VAULT :
   - Fiche analyse : 05-ANALYSES\YYYY-MM-DD_analyse-[wallet].md
   - Si qualified : 03-STRATEGIES\strategie-[type]-v[X].md
   - Màj SCHEMAS-RUGGERS si nouveau pattern
   - Màj correlations.md si corrélation trouvée

8. VERDICT FINAL :
   - GO / NO GO / PAPER TRADING
   - Config exacte à appliquer
   - Risques identifiés
---

---

## 🚀 DÉBUT DE SESSION (copier-coller)

SESSION TRADING — Démarrage
CHARGE LE CERVEAU FPROJECT :
fproject_brain({section:"voice"})
fproject_brain({section:"kernel"})
fproject_brain({section:"smart-core"})
RELIS MON VAULT via MCP Filesystem :
C:\TradingBot\00-SYSTEM\PROMPT-SYSTEM.md
C:\TradingBot\02-RUGGERS\SCHEMAS-RUGGERS.md
C:\TradingBot\06-ERREURS\erreurs-recurrentes.md
C:\TradingBot\07-PERFORMANCE\journal-PnL.md
RÉSUME-MOI :
Mon PnL actuel (journalier/cumulé)
Mes ruggers actifs et leurs configs
Mes erreurs à ne pas répéter
L'état du marché aujourd'hui
QUE FAISONS-NOUS AUJOURD'HUI ?
plain

---

## 🔍 ANALYSER UN TOKEN/DEV (copier-coller)
ANALYSE CE TOKEN/DEV
Adresse : [METS L'ADRESSE ICI]
Deep dig Fproject (cex_research ou qualify)
Type de rugger ?
Config proposée ?
GO ou NO GO ?
Écris l'analyse dans le vault.
plain

---

## 🎯 TROUVER UN RUGGER (copier-coller)
TROUVE-MOI UN RUGGER À SNIPE
Easy Snipe Fproject
Si trouvé : type, config, GO/NO GO
Si rien : pourquoi, quoi surveiller
Écris dans le vault si trouvé.
plain

---

## 🔍 ANALYSER UN WALLET + SIMULATION (copier-coller)
ANALYSE WALLET + SIMULATION
Adresse : [METS L'ADRESSE ICI]
Deep dig Fproject (wallet + qualify + candles)
Entry blocks / placement / copytrade_score
Config optimale (TP/SL/buy amount)
Simulation sur 20-30 derniers tokens
Verdict GO/NO GO / PAPER TRADING
Écris tout dans le vault (analyse + stratégie)
plain

---

## 💰 PORTFOLIO & SELL (copier-coller)
ÉTAT DU PORTFOLIO
Portfolio overview Fproject
Positions ouvertes — lesquelles sell ?
PnL actuel
Stop atteint ?
Écris la mise à jour PnL dans le vault.
plain

---

## 📝 ARCHIVER UNE SESSION (copier-coller à la fin)
ARCHIVE CETTE SESSION
Écris dans le vault :
Trade exécuté ? → 04-TRADES\YYYY-MM\YYYY-MM-DD_trade-XXX.md
Erreur détectée ? → 06-ERREURS\erreur-XXX.md + erreurs-recurrentes.md
Nouveau rugger/pattern ? → 02-RUGGERS\SCHEMAS-RUGGERS.md
Stratégie validée ? → 03-STRATEGIES\strategie-[type]-v[X].md
Analyse approfondie ? → 05-ANALYSES\YYYY-MM-DD_analyse-[token].md
Màj PnL → 07-PERFORMANCE\journal-PnL.md
Confirme chaque fichier écrit.
plain

---

## ❌ ARCHIVER UNE ERREUR (copier-coller)
ARCHIVE CETTE ERREUR
Token : [ADRESSE]
Montant perdu : [$X]
Description : [QUE S'EST-IL PASSÉ]
Écris :
06-ERREURS\erreur-XXX.md
Màj 06-ERREURS\erreurs-recurrentes.md
Confirme.
plain

---

## 📊 MÀJ PNL (copier-coller)
MÀJ PNL
Date : [DATE]
Trades aujourd'hui : [X]
Gains : [
X]Pertes:[
 
X]
PnL jour : [+X/− X]
Écris dans 07-PERFORMANCE\journal-PnL.md
plain

---

## ⚡ RACCOURCIS RAPIDES

| Tu veux... | Tu dis... |
|-----------|-----------|
| Démarrer | `SESSION TRADING — Démarrage` |
| Analyser token | `ANALYSE [ADRESSE]` |
| Analyser wallet | `ANALYSE WALLET [ADRESSE]` |
| Trouver rugger | `TROUVE-MOI UN RUGGER` |
| Portfolio | `PORTFOLIO` |
| Sell | `SELL [TOKEN] [X%]` |
| Setup tracker | `SETUP TRACKER [ADRESSE]` |
| Archiver session | `ARCHIVE CETTE SESSION` |
| Archiver erreur | `ARCHIVE CETTE ERREUR` |
| Màj PnL | `MÀJ PNL` |

---

## 🎯 RÈGLES EN 1 LIGNE

- **150$ max** par trade
- **-250$ stop** journalier
- **Pas de martingale**
- **Paper trading 48h** avant vrai argent
- **Validation humaine** avant tout trade

---

> 💡 **Astuce** : Garde ce fichier ouvert dans Obsidian pendant tes sessions.
🔄 SYNC GITHUB
N'oublie pas :
plain
Ctrl + P → "Obsidian Git: Commit and push"