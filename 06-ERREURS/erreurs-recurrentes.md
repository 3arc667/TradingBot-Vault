# ❌ ERREURS À NE PAS RÉPÉTER

> ⚠️ Relire ce fichier avant chaque session de trading

---

## 🚨 CRITIQUES (arrêt immédiat)

| # | Erreur | Date 1ère | Date dernière | Correction | Vérifié |
|---|--------|-----------|---------------|------------|---------|
| C1 | Config activée en live sans finir les 48h paper (E7T1Vs) | 2026-08-13 | 2026-08-15 | Gate paper strict ; ordre de bascule seulement après 48h + ≥20 lancements + validation humaine | ☐ |

---

## ⚠️ MAJEURES (alerte avant trade)

| # | Erreur | Date 1ère | Date dernière | Correction | Vérifié |
|---|--------|-----------|---------------|------------|---------|
| 1 | Claude a proposé 3 configs TP différentes (150%, 100%, 70%) sur même rugger | 2026-08-10 | 2026-08-12 | Vault structuré + stratégies versionnées | ☐ |
| 4 | Reformuler un setup rejeté sous un nouvel angle pour obtenir un autre verdict | 2026-08-13 | 2026-08-15 | Tenir le verdict structurel ; l'angle change, la règle non | ☐ |

---

## ℹ️ MINEURES (optimisation)

| # | Erreur | Date 1ère | Date dernière | Correction | Vérifié |
|---|--------|-----------|---------------|------------|---------|
| 3 | Petit échantillon manuel traité comme backtest (biais de sélection) | 2026-08-13 | 2026-08-15 | Journal manuel = couleur, pas mesure ; mesure = desk/paper | ☐ |
| 5 | Backtest bougie relancé alors que l'outil ne remonte pas jusqu'à l'entrée | 2026-08-15 | 2026-08-15 | Ne pas relancer à l'aveugle ; fills TP mesurés en paper (voir erreur-005.md) | ☐ |

---

## 📝 Journal des corrections

| Date | Erreur # | Action | Résultat |
|------|----------|--------|----------|
| 2026-08-15 | C1 | Refus répété d'activer BxLm/wallet 01 en live ; paper lancé à la place | Ligne tenue |
| 2026-08-15 | 5 | 2 tokens testés, couverture d'entrée absente → backtest bougie abandonné | Documenté |
