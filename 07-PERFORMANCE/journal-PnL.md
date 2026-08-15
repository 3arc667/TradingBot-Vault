# 📊 JOURNAL PnL — Suivi quotidien

## 🎯 Objectifs mensuels

- **Objectif PnL** : +$500
- **Max perte acceptée** : -$500
- **Winrate visé** : > 55%

---

## 📅 2026-08

| Date  | Trades | Gains  | Pertes | PnL jour | PnL cumulé | Stop atteint ? |
| ----- | ------ | ------ | ------ | -------- | ---------- | -------------- |
| 08-12 | —      | —      | —      | —        | —          | pas de données |
| 08-13 | —      | —      | —      | —        | —          | pas de données |
| 08-14 | 1      | $7.43  | $0     | +$7.43   | +$7.43     | non (partiel — fenêtre 24h) |
| 08-15 | 11     | $72.92 | $2.87  | +$70.04  | +$77.47    | non            |

**Total mois (trades loggés — scope 24h)** : +$77.47  
**Winrate** : 91.7 % (11 W / 1 L sur 12)  
**PnL net (scope 24h)** : +$77.47

> ⚠️ Scope : ce total couvre uniquement la fenêtre 24h (14/08 16:22 → 15/08 16:22).
> Non capturés ici : 2 gros rugs du 14/08 (−86 % $Wrpu, −98 % $8fLy) sortis avant le cutoff.
> Sur 72h le net réel desk est −$26.01 (29 W / 18 L). À compléter si on veut le mois complet.

---

## 📊 Détail par wallet — fenêtre 24h (SOL $75.43)

| Wallet | Trades | W/L | PnL SOL  | PnL $   |
| ------ | ------ | --- | -------- | ------- |
| 01 (8Kh2…ksCt) | 6  | 6/0 | +0.6007 | +$45.31 |
| 02 (4g5B…KkKy) | 2  | 1/1 | +0.0494 | +$3.72  |
| 04 (B37U…LBtF) | 4  | 4/0 | +0.3770 | +$28.44 |
| **Total**      | 12 | 11/1| +1.0271 | +$77.47 |

## 📋 Détail par trade — fenêtre 24h

| Clôture (UTC) | Token | Wallet | PnL % | PnL SOL |
| ------------- | ----- | ------ | ----- | ------- |
| 08-15 08:01 | $TBQ | 01 | +22 | +0.0943 |
| 08-15 08:01 | $TBQ | 04 | +22 | +0.0878 |
| 08-15 07:33 | $fomoguy | 01 | +33 | +0.1406 |
| 08-15 07:33 | $fomoguy | 04 | +25 | +0.1017 |
| 08-15 06:49 | $pumpsem | 01 | +23 | +0.0988 |
| 08-15 06:49 | $pumpsem | 04 | +26 | +0.1036 |
| 08-15 06:49 | $pumpsem | 02 | +26 | +0.0875 |
| 08-15 06:15 | $bad call | 01 | +15 | +0.0620 |
| 08-15 06:15 | $bad call | 04 | +21 | +0.0838 |
| 08-15 05:28 | $CANDLECRY | 01 | +25 | +0.1065 |
| 08-15 05:28 | $CANDLECRY | 02 | −11 | −0.0381 |
| 08-14 16:28 | $Gw7U | 01 | +21 | +0.0985 |

_MàJ : 2026-08-15 · source : desk Fproject (portfolio 24h) · 0 position ouverte_

---

## 📈 Graphique (manuel ou via Dataview)

```dataview
TABLE date, pnl_jour, pnl_cumule
FROM "04-TRADES"
SORT date ASC
```

> 💡 **Astuce** : Active le plugin Dataview dans Obsidian pour des tableaux auto
