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

## 🔁 Run ring E7T1Vs / BxLm — 2026-08-16 (SOL $75.41)

> Collecte live, 2 wallets encore armés au moment du run (avant régularisation C1).
> w04 = E7T1Vs (entrée ~0.404), w01 = BxLm (entrée ~0.504).

| Token | CA (court) | w04 E7T1Vs | w01 BxLm |
| ----- | ---------- | ---------- | -------- |
| $CATU | 679up6… | +69% | +34% |
| $RM | 3ykPgE… | +59% | +22% |
| $Dockey | BfafhZ… | +56% | +31% |
| $FOMOANSEM | 95Csmx… | −12% (auto, sortie molle) | **+24% (close MAIN Akeno)** |
| $Tonguuue | Eks774… | −100% (rug) | −97% (rug) |

**Lecture à froid :** 6 tokens — 4 verts francs, 1 mixte, 1 rug total.
- TP étagé E7T1Vs laisse courir (+69/+59/+56) vs BxLm flat (+34/+22/+31).
- $Tonguuue −100% = donnée normale sur snipe de rugger, PAS un bug. A motivé le SL −75.
- Close manuelle Akeno sur $FOMOANSEM (w01, +24%) : **notée comme couleur, pas comme mesure** (échantillon = 1, cf. erreur-003). Ne prouve pas main > auto.

**Post-run :** BxLm désarmé, E7T1Vs (w04) seul armé + SL −75 posé. Voir strategie-copytrade-E7T1Vs-v2.md.

_MàJ : 2026-08-16 · source : desk Fproject (positions closed) · 0 position ouverte_

---

## 🔁 Session 2026-08-16 (soir) — closes ring + état trackers réel (SOL $75.24)

> Voir 04-TRADES/2026-08/2026-08-16_trade-001.md pour le détail.

**Nouveaux closes (hors run précédent)** : net ≈ **−0.986 SOL ≈ −$74.2**.

| Token | w04 (B37U) | w01 (8Kh2) |
| ----- | ---------- | ---------- |
| $plumbercat | −94% | −100% |
| $PLUNGER | +14% | −8% |
| $ActPepe | +35% | — |
| $DORAIN | −75% | −13% |

### ⚠️ Découvertes (état trackers = source autoritaire)
1. **Double-buy C1 FERMÉ (soir, après vérif trackers).** w04 (B37U) a coupé son autoBuy sur 3 pertes d'affilée. Reste 1 seul acheteur E7T1Vs = w01. ⚠️ mais w01 = le wallet **sans SL** → risque résiduel à corriger.
2. **Config live ≠ vault.** Les 2 trackers E7T1Vs qui achètent sont à **TP +33/+35% + sortie MC ~46,5–49,5k**, PAS le 50/120. Le 50/150 étagé est sur le tracker adresse BxLm, **désarmé** (autoBuy off). Le "+50/+120 qui saigne" ne correspond pas à ce qui s'exécute.
3. **SL incohérent.** Tracker w01 = SL OFF. Tracker w04 = SL −75. Même rugger, deux configs.
4. **DqTG8k** = observation (autoBuy off), tp33/SL75/MC51250 ; ne partage que 2 tokens avec E7T1Vs → wallet largement indépendant (vérif Akeno confirmée).

### Décisions en attente Akeno (aucune modif faite)
- ~~Fermer le double-buy~~ ✅ fait. **Poser un SL sur w01** (seul armé, sans stop) = priorité #1.
- Trancher le TP une fois le fill mesuré (voir 05-ANALYSES/2026-08-16_analyse-fill-E7T1Vs.md).
- Lancer le test TSL@40k (05-ANALYSES/2026-08-16_protocole-test-TSL-40k.md).

_MàJ : 2026-08-16 (soir) · source : desk Fproject (positions closed + trackers) · 0 position ouverte_

---

## 📈 Graphique (manuel ou via Dataview)

```dataview
TABLE date, pnl_jour, pnl_cumule
FROM "04-TRADES"
SORT date ASC
```

> 💡 **Astuce** : Active le plugin Dataview dans Obsidian pour des tableaux auto
