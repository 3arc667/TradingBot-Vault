# ❌ ERREURS À NE PAS RÉPÉTER

> ⚠️ Relire ce fichier avant chaque session de trading

---

## 🚨 CRITIQUES (arrêt immédiat)

| # | Erreur | Date 1ère | Date dernière | Correction | Vérifié |
|---|--------|-----------|---------------|------------|---------|
| C1 | Config activée en live sans finir les 48h paper (E7T1Vs) | 2026-08-13 | 2026-08-16 | Gate paper strict ; ordre de bascule seulement après 48h + ≥20 lancements + validation humaine. **2026-08-16 : régularisé** — desk n'a pas de vrai mode paper, dérogation assumée = 1 seul wallet live borné (E7T1Vs w04, SL −75), backup BxLm coupé | ☑ |

---

## ⚠️ MAJEURES (alerte avant trade)

| # | Erreur | Date 1ère | Date dernière | Correction | Vérifié |
|---|--------|-----------|---------------|------------|---------|
| 1 | Claude a proposé 3 configs TP différentes (150%, 100%, 70%) sur même rugger | 2026-08-10 | 2026-08-12 | Vault structuré + stratégies versionnées | ☐ |
| 4 | Reformuler un setup rejeté sous un nouvel angle pour obtenir un autre verdict | 2026-08-13 | 2026-08-15 | Tenir le verdict structurel ; l'angle change, la règle non | ☐ |
| 6 | TP étagé non backtesté (50/120) déployé live sur E7T1Vs. Diagnostic initial faux (« +120 hors de portée, max +69 ») tiré de 6 tokens = erreur-003 reproduite. Mesure 72h (n=46) : +120 atteint 43%, pic médian +102%. Vrai défaut = fill réel < pic atteignable (timing rug bloc-0), pas la cible | 2026-08-16 | 2026-08-16 | Mesurer le fill sur closes live (n≥20), ne pas déduire de l'ATH ; arbitrage TP à Akeno (voir erreur-006.md + 05-ANALYSES/2026-08-16_analyse-fill-E7T1Vs.md) | ☐ |

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
| 2026-08-16 | C1 | Découvert : E7T1Vs + BxLm tournaient en live sous label paper (double-buy sur le ring). Régularisé : BxLm désarmé, E7T1Vs seul live borné + SL −75. Dérogation actée par Akeno | Écart fermé, dérogation documentée |
| 2026-08-16 | 6 | Akeno signale que le TP étagé 50/120 saigne. Confirmé : jamais backtesté, 2e tranche hors distribution ring. erreur-006 créée, arbitrage TP en attente | Ouverte |
| 2026-08-16 | 6 | Mesure fill 72h (n=46) tirée : +120 atteint 43%, pic médian +102% → mon diagnostic « +69 plafond » (6 tokens) était faux, erreur-003 reproduite et corrigée. Vrai blocker = fill réel < atteignable | Corrigé |
