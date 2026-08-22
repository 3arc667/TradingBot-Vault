# 🎭 SCHÉMAS DES RUGGERS — Base de connaissances

> ⚠️ **Ce fichier est la BIBLE.** Claude doit le relire avant chaque classification.

## 📊 Tableau récapitulatif

| Type | Nom            | Pattern                   | Durée typique | Danger                                                         | Stratégie                      |
| ---- | -------------- | ------------------------- | ------------- | -------------------------------------------------------------- | ------------------------------ |
|      | FAX4qRQ…J1aqp  | Multi-token same-address  |               | 8 tokens sortis d'une seule adresse                            | ⛔ REJECT (banni)               |
|      | 241nHsSE…jBny2 | Ring 2-wallets            |               | mother-funder non-CEX2 wallets frères alternent les lancements | Aucune⛔ NO GO (funding opaque) |
|      | AoGefnxF…McMFe | Spam machine mono-adresse |               | 12 tokens en 31h, funding mother non-CEX                       | Aucune	⛔ NO GO (EV négatif)    |
| D    | Ring E7T1Vs/BxLm/DqTG8k | Copytrade — devs jetables CEX-financés | ~35 MC entrée | devs varient, ring constant ; land-contention | 🟡 COPYTRADE ring (E7T1Vs), PAPER |
| E    | BJgZGd (coffre) → distributeurs → 1000 wallets | Machine distribution/bundle industrielle | rotation continue | 3 étages jetables, feuilles non-créatrices | ⛔ INTRACKABLE (blindage) |
| B★   | Binance 5tzFki + 3.989 | 3.989 = montant standard (92,7% sorties, 881 dest./2mois) ; usine à launches | ~15/j | ~50% DUMP (profil AoGef) ; runners jusqu'à 43k | 🔴 PAS un tracker propre — snipe à plat NON ; filtre anti-rug + PAPER seulement |

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

## 🟢 TYPE D — Ring copytrade (constante = le wallet, pas le dev)

### Caractéristiques
- Un ring de wallets bundler snipe block-0 des tokens de **devs jetables**, un token par dev.
- Devs financés par **CEX variés** (KuCoin, Binance HW2, MEXC), montants **précis mais différents à chaque fois**.
- Aucun montant réutilisé → **pas de signature CEX+montant** → pas de tracker Méthode 1 par dev.
- La constante exploitable = le **wallet du ring** qui les snipe tous.

### Cas confirmés (2026-08-15)
- Dev HB22Qt (DG1Bi) → KuCoin, 7,255542 SOL — lié au ring.
- Dev SMshZ (3qvr) → Binance HW2, 5,855502 SOL — lié au ring.
- Ring : E7T1Vs (référence, block-0 99,7%), BxLm (jumeau/backup), DqTG8k (land-late 72% → out).

### Règle
- **Copytrader le ring, pas courir après chaque dev.** Une seule référence (E7T1Vs).
- Tracker le hot wallet CEX = erreur-002 (le CEX est le départ, pas la cible).
- Validation = paper (fills TP), pas backtest bougie (erreur-005).

### Stratégie associée
→ `03-STRATEGIES/strategie-copytrade-E7T1Vs-v2.md` (LIVE borné — réf unique w04 + SL −75)

### État live RÉEL (2026-08-16 soir — corrigé sur trackers, source autoritaire)
> ⚠️ L'état précédent (« E7T1Vs w04 seul armé, BxLm désarmé ») était FAUX. Photo trackers réelle :
- **E7T1Vs — double-buy FERMÉ (2026-08-16 soir)** — update trackers :
  - w04 (B37U) : autoBuy **OFF** (coupé après 3 pertes d'affilée). Garde SL −75 + sortie MC 49,5/55,5k, délai 2s. N'achète plus.
  - w01 (8Kh2) : autoBuy **ON** — **seul acheteur E7T1Vs**. TP +35% / sortie MC 46 500, délai 1,5s, buy 0.4. ⚠️ **SL OFF** — le wallet encore armé est celui sans stop. À corriger en priorité.
- **Tracker adresse BxLm** (BxLmrDJa…) : autoBuy OFF (n'achète pas). C'est LUI qui porte le TP étagé 50@+50 / 100@+150 + SL −75 — donc le « 50/120 » du vault ne s'exécute pas.
- **DqTG8k** : observation (autoBuy OFF), tp33 / SL75 / MC51250, wallet w02 (4g5B). Ne partage que **2 tokens** avec E7T1Vs (lien faible) → **wallet largement indépendant**, pas un jumeau du ring. Rapport profond à finir (analyste occupé 3×).

### À trancher (Akeno) — aucune modif faite
- ~~Fermer le double-buy~~ ✅ fait (w04 coupé). **Poser un SL sur w01** (seul armé, actuellement sans stop) = priorité #1.
- TP définitif après mesure du fill (05-ANALYSES/2026-08-16_analyse-fill-E7T1Vs.md).
- Test TSL@40k : protocole posé (05-ANALYSES/2026-08-16_protocole-test-TSL-40k.md) — à lancer sur ≥20 closes.
- Statuer DqTG8k : indépendant → tracker séparé ou out ?

---

## ⚫ TYPE E — Machine de distribution / bundle industrielle (intrackable)

### Caractéristiques
- Structure à 3 étages, tous jetables : **coffre** (agrège le bénéf du ring) → **distributeurs** (200–800 SOL, tournent) → **1000+ wallets frais** (1–5 SOL chacun).
- Les feuilles **ne créent AUCUN token** (bundle/makers ou dispatch, pas des launchers).
- Volume massif et rapide : ex. 1 distributeur = 1000 wallets armés + 2 543 SOL en 1h20.
- Chaque étage jetable = conçu pour être **intrackable**.

### Test de tri (réflexe)
- Le fric qui **REMONTE** vers un gros wallet qui agrège = cash-out. **Jamais un tracker.**
- Le fric qui **DESCEND** vers des wallets frais **QUI LANCENT** = mère trackable.
- Question unique : *les enfants créent-ils des tokens ?* Non → intrackable, on lâche.

### Cas confirmé (2026-08-22)
- Coffre BJgZGd (885+) → 63 distributeurs (paires ~750+~200/250) → distributeur 8txZUG
  arme 1000 feuilles (2 543 SOL / 1h20), feuilles = 0 token créé.
- Seul maillon actionnable = le **top-trader source (8tfUh)**, en copytrade Method 2.
- Détail : `05-ANALYSES/2026-08-22_analyse-ring-bundle-BJgZGd.md`

### Stratégie associée
→ ⛔ Pas de tracker sur le ring. Remonter au trader source prouvé et le qualifier en copy.

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

| Date       | Token | Type initial   | Type final | Confiance                                                                | Notes                                    |
| ---------- | ----- | -------------- | ---------- | ------------------------------------------------------------------------ | ---------------------------------------- |
| 2026-08-13 | -     | FAX4qRQ…J1aqp  | NO GO      | REJECT Fproject. Multi-token même adresse = banni                        | WR 75% mais rétroviseur, pas prédictif.  |
| 2026-08-13 | -     | 241nHsSE…jBny2 | NO GO      | pas de signature réutilisable,pattern_holds=false. Mother-wallet non-CEX | WR 66% mais source funding non traçable  |
| 2026-08-13 | -     | AoGefnxF…McMFe | NO GO      | 2 winners masquent 7 morts (survivor bias).                              | EV −2,2%, WR 41,7%. Spam 12 tokens/31h.  |
| 2026-08-15 | -     | Ring E7T1Vs/BxLm/DqTG8k | TYPE D — COPYTRADE ring (PAPER) | Block-0 99,7% (E7T1Vs/BxLm) ; DqTG8k 72% out | Devs CEX-financés varié, pas de tracker/dev. Copytrade-ring confirmé. |
| 2026-08-22 | -     | Ring BJgZGd (coffre) | TYPE E — INTRACKABLE | Feuilles 0 token créé ; 3 étages jetables | Distribution/bundle industrielle. Seul actionnable = trader source 8tfUh (copy). |
| 2026-08-22 | POSSWACK | Signature Binance 5tzFki/3.989 | 🔴 REJET tracker propre (à plat) | 3.989 = 92,7% des sorties, 881 dest./2mois ; sample 10 tokens ~50% dump | Usine à launches mais profil AoGef (pile ou face). "2/2 winners" = survivor bias (erreur-008). Filtre anti-rug + PAPER seulement. Voir 05-ANALYSES/2026-08-22_analyse-signature-binance-3989.md |
