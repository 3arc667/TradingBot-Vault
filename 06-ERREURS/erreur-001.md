---
date: 2026-08-10
id: erreur-001
gravite: MAJEURE
type: Config
recurrence: RÉCURRENT
---

## 🚨 Description

Claude a proposé 3 configurations différentes pour le même type de rugger :
- Config 1 : TP à 150%
- Config 2 : TP à 100%
- Config 3 : TP à 70%

Sans structure claire, Claude s'est "embrouillé" dans les fichiers mémoire et a changé d'avis à chaque session.

## 🔍 Cause racine

- Pas de vault structuré pour stocker les configs validées
- Chaque session = nouvelle analyse sans mémoire des précédentes
- Pas de stratégie versionnée par rugger

## 💸 Impact PnL

- Perte estimée due à des configs incohérentes : -$XXX (à compléter)
- Confiance perdue dans les recommandations de Claude

## ✅ Correction appliquée

1. Création du vault Obsidian structuré
2. Une stratégie = un fichier versionné dans 03-STRATEGIES/
3. Avant de proposer une config, relire la dernière version validée
4. Documenter chaque changement de config comme une nouvelle version

## 🔒 Vérification

- [x] Vault Obsidian créé
- [x] Templates créés
- [ ] Paper trading 48h sur nouvelle structure
- [ ] Prochaine session : vérifier que Claude relit les stratégies avant de proposer

## 📎 Liens

- Stratégie concernée : 03-STRATEGIES/strategie-[type]-v1.md (à créer)