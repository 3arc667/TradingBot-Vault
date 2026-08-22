# ❌ ERREURS À NE PAS RÉPÉTER

> ⚠️ Relire ce fichier avant chaque session de trading

---

## 🚨 CRITIQUES (arrêt immédiat)

| # | Erreur | Date 1ère | Date dernière | Correction | Vérifié |
|---|--------|-----------|---------------|------------|---------|
| C1 | Config activée en live sans finir les 48h paper (E7T1Vs) + double-buy | 2026-08-13 | 2026-08-16 | **Double-buy FERMÉ 2026-08-16 (soir)** : w04 (B37U) a coupé son autoBuy (3 pertes d'affilée = maxConsecutiveLosses). Reste **1 seul acheteur E7T1Vs = w01 (8Kh2)**. ⚠️ **RISQUE RÉSIDUEL** : le wallet encore armé (w01) n'a **AUCUN SL** (celui coupé, w04, avait le SL −75). Rug pré-40k sur w01 = −100%. À corriger : poser SL sur w01. Gate paper 48h toujours non tenu (dérogation) | ☐ |

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
| 7 | Verdict desk "dead/stale / n=0" pris pour argent comptant sur un wallet ACTIF (GDQeTnqk : +54 SOL / 9j, 1000 swaps) — trou d'index Terminal | 2026-08-22 | 2026-08-22 | "dead/stale" du desk ≠ inactif. Vérifier l'export DeFi on-chain (Solscan) avant de classer un wallet mort | ☐ |
| 8 | Signature CEX déclarée "confirmée / tracker candidat" sur 2 launches gagnants (3.989) — survivor bias. CSV complet : 3.989 = 92,7% des sorties du wallet, 881 dest./2mois, ~50% dump (profil AoGef) | 2026-08-22 | 2026-08-22 | Hair-thin ne vaut que si le montant est RARE : compter les destinataires dans le CSV avant de valider une signature. Échantillon réparti (pas 2 tokens choisis) avant tout verdict tracker | ☐ |
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
| 2026-08-16 | C1 | État trackers réel lu : double-buy E7T1Vs (w01+w04 autoBuy) TOUJOURS actif ; config live = TP +33/35 + MC (pas 50/120, qui est sur tracker BxLm désarmé) ; w01 sans SL. C1 rouvert, corrections à valider par Akeno | Rouvert |
| 2026-08-16 | C1 | Akeno a coupé le double-buy (w04 autoBuy off après 3 pertes). Vérifié trackers : 1 seul acheteur E7T1Vs = w01. Mais w01 = celui SANS SL → risque résiduel, SL à poser | Double-buy fermé, SL w01 à faire |
| 2026-08-22 | 7 | GDQeTnqk qualifié "dead/stale" par le desk ; export on-chain fourni par Akeno → wallet très actif (63,5% WR, +54 SOL/9j). Analyse refaite sur CSV | Corrigé ; réflexe CSV-avant-verdict-mort acté |
| 2026-08-22 | 8 | Plage 3.989 vendue comme "tracker confirmé" sur 2 winners ; Akeno signale des instant-rugs ; CSV + échantillon 8 wallets → ~50% dump, 3.989 = montant standard (881 dest.). Rétrogradée en REJET (à plat) | Corrigé ; survivor bias reconnu, filtre anti-rug + paper requis |
