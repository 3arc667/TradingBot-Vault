---
date: 2026-08-15
type: analyse-ring-copytrade
ring: "block-0 twins (Binance/KuCoin funded)"
wallets:
  - E7T1Vs7aCLkN7TyFg382rhG7yVM5cWvjuwhfQkWPiSEH
  - BxLmrDJaNr9hA35FBGASAhUK74Gs98AyvQXx6HSR1Qft
  - DqTG8k1SSuXUnbLLr17pvPK8iKwjaARqqeRSsPmeNgeU
source: desk Fproject (rapports wallet) + données manuelles Akeno (2026-08-13)
statut: référence choisie = E7T1Vs (PAPER)
---

# Analyse ring copytrade — E7T1Vs / BxLm / DqTG8k

## 1. Comparaison géométrie d'entrée (seul critère copy)

| Métrique | E7T1Vs | BxLm | DqTG8k |
|---|---|---|---|
| Block 0 | 99,7% | 99,7% | **72%** |
| Block 0/+2 | 99,7% | 99,7% | 86% |
| Médiane entrée | +0 | +0 | +0 |
| Score copy | 75 | 75 | 75 |
| Score rugger | 83 | 83 | 65 |
| Tokens tradés | 656 | 656 | 512 |
| Financement | Binance HW2 | KuCoin | Binance HW2 (profondeur 2) |
| Type | unresolved_forward | atomic_relay | normal |

## 2. Verdict

- **E7T1Vs → RÉFÉRENCE du ring.** Block-0 quasi parfait, déjà copy wallet 1.
- **BxLm → jumeau, BACKUP.** Géométrie identique. Même ring → copier les deux = **2 buys par lancement** sur le même token. On garde UN seul. Ne pas activer BxLm en 2ᵉ live.
- **DqTG8k → REJECT copy.** Block-0 seulement 72%, arrive en retard ~28% du temps (block_delta jusqu'à +236 sur certains). Bon trader en PnL réalisé, mais l'entrée est sous les jumeaux. En copy on achète l'entrée → out.

**Règle du ring appliquée : une seule référence = E7T1Vs.**

## 3. Croisement avec les données manuelles d'Akeno (2026-08-13)

Log manuel E7T1Vs : **8 TP touchés / 9** → même direction que le desk (cible forte). ✅

Écart de magnitude (ATH manuel vs ATH copytrade desk) :

| Token | ATH manuel | ATH copytrade desk |
|---|---|---|
| GD758yo | 56 | 58 ✓ |
| 8aUQdg | 73,9 | 78 (proche) |
| Yb4vUY | 82 | 98 |
| 3qvrZEd | 73 | 152 |
| DG1Biazy | 96 | 182 |
| 8eisWDF | 5 (raté) | 31 |

→ Journal manuel fiable en **direction**, pas en **magnitude** (erreur-003). Mesure de référence = desk (`ath_pct_copytrade`). Log manuel = couleur.

## 4. Insight config d'Akeno
- **"Délai copytrade 2s recommandé"** : entrer ~2s après le wallet = on ne court plus le block-0 → **contourne en partie le risque de landing/contention**. À tester en paper comme variante de la config E7T1Vs.

## 5. Holds (non rouverts)
- **FAX** (`FAX4qRQ…`) : reste BANNI. 14 tokens sur une adresse dans le log manuel = trigger de ban confirmé. Le journal ne rouvre pas un verdict structurel (erreur-004).
- **6GKHVwqR** : log manuel 6/7 gagnants, mais desk = coupé (score copy ~0). Petit échantillon manuel = biais de sélection. Coupe maintenue.

## 5bis. Analyse financement des devs (2026-08-15, lead Akeno)

Fouille de 2 devs sniperés par le ring :

| Dev (token) | Financé par | Montant |
|---|---|---|
| HB22Qt (DG1Bi) | KuCoin | 7,255542 SOL |
| SMshZ (3qvr) | Binance HW2 | 5,855502 SOL |

**Constat (confirme l'observation d'Akeno)** : CEX différent à chaque fois, montants précis mais **jamais identiques**. Aucun montant réutilisé → **pas de signature CEX+montant** → pas de tracker Méthode 1 par dev. Tracker le hot wallet CEX = erreur-002.

**Trouvaille clé** : les 2 devs sont liés au **même ring** (BxLm / E7T1Vs / DqTG8k / 2LLHCt / AQVoC). Les devs changent, le ring reste. → **copytrade-ring confirmé comme la bonne méthode**, sniping par dev écarté (nouveau TYPE D dans SCHEMAS-RUGGERS).

**Limite** : la piste de financement n'apporte PAS le chemin de prix → ne débloque pas le backtest bougie (erreur-005). Levier différent.

## 6. Suite
- Référence ring = E7T1Vs → strat `03-STRATEGIES/strategie-copytrade-E7T1Vs-v1.md` (PAPER).
- Variante à paper-trader : délai 2s.
- Gate inchangé : 48h paper + ≥20 lancements/72h + validation humaine avant live.
