# 🎭 SCHÉMAS DES RUGGERS — Base de connaissances

> ⚠️ **Ce fichier est la BIBLE.** Claude doit le relire avant chaque classification.

## 📊 Tableau récapitulatif

| Type | Nom            | Pattern                  | Durée typique | Danger                              | Stratégie        |
| ---- | -------------- | ------------------------ | ------------- | ----------------------------------- | ---------------- |
|      | FAX4qRQ…J1aqp  | Multi-token same-address |               | 8 tokens sortis d'une seule adresse | ⛔ REJECT (banni) |
|      | 241nHsSE…jBny2 | Ring 2-wallets           |               |                                     |                  |

---

## 🟡 TYPE A — Slow Rug

### Caractéristiques
- Distribution des tokens : 40-60% chez le dev
- Liquidity pool : verrouillée 24-48h
- Volume : croissant puis chute progressive
- Communauté : active au début, puis silence

### Signaux MCP Fproject
- [ ] Fonds du dev non retirés immédiatement
- [ ] Plusieurs wallets liés au dev
- [ ] Transactions de test avant launch

### Stratégie associée
→ `03-STRATEGIES/strategie-type-A-v[X].md`

---

## 🔴 TYPE B — Instant Dump

### Caractéristiques
- Distribution : 70-90% chez le dev
- Dump : block 3 à block 10
- Volume : pic immédiat puis crash
- Pas de communauté

### Signaux MCP Fproject
- [ ] Fonds du dev prêts à être retirés
- [ ] Wallet unique ou peu de wallets
- [ ] Aucune transaction de test

### Stratégie associée
→ `03-STRATEGIES/strategie-type-B-v[X].md`

---

## 🔴 TYPE C — Honey Pot

### Caractéristiques
- On peut acheter mais PAS vendre
- Code malveillant dans le smart contract
- Prix artificiellement haut
- Aucune liquidité réelle

### Signaux MCP Fproject
- [ ] Fonction de vente désactivée
- [ ] Contract audité = FAIL
- [ ] Pas de liquidité retirable

### Stratégie associée
→ **NE PAS TRADER** — Éviter totalement

---

## ⚫ TYPE ? — Inconnu

### Quand classifier ici :
- Nouveau pattern jamais vu
- Données MCP Fproject insuffisantes
- Comportement atypique

### Action
1. Paper trading obligatoire
2. Documenter dans `05-ANALYSES/patterns-emergents.md`
3. Attendre 3-5 cas similaires pour créer un nouveau type

---

## 📝 Journal de classification

| Date | Token | Type initial | Type final | Confiance | Notes |
| ---- | ----- | ------------ | ---------- | --------- | ----- |
|      |       |              |            |           |       |
