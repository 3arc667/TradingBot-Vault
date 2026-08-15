
🚀 DÉBUT DE SESSION
---

SESSION TRADING — DÉMARRAGE

1. Relis mon vault GitHub :
   https://raw.githubusercontent.com/3arc667/TradingBot-Vault/main/00-SYSTEM/PROMPT-SYSTEM.md
   https://raw.githubusercontent.com/3arc667/TradingBot-Vault/main/02-RUGGERS/SCHEMAS-RUGGERS.md
   https://raw.githubusercontent.com/3arc667/TradingBot-Vault/main/06-ERREURS/erreurs-recurrentes.md
   https://raw.githubusercontent.com/3arc667/TradingBot-Vault/main/05-ANALYSES/correlations.md

2. Résume mes ruggers connus, mes erreurs, mes corrélations actives.

3. Qu'est-ce que tu proposes aujourd'hui ?

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
## 🤖 SESSION AVEC ÉCRITURE AUTO
SESSION TRADING — Écriture automatique activée
Relis mon vault via MCP Filesystem
[TA DEMANDE : analyse token / trouver rugger / portfolio]
Écris TOI-MÊME les conclusions dans le vault :
Trade → 04-TRADES\
Erreur → 06-ERREURS\
Analyse → 05-ANALYSES\
Stratégie → 03-STRATEGIES\
PnL → 07-PERFORMANCE\
Confirme-moi chaque fichier écrit
Je ferai le commit/push GitHub après

---
🔍 PROMPT ANALYSE WALLET + SIMULATION
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