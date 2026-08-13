---
date: 2026-08-13
id: erreur-004
gravite: MAJEURE
type: Analyse
recurrence: RÉCURRENT
---

## 🚨 Description

Troisième tentative de faire passer le dev `FAX4qRQdiSj2iWDYvkJ21VieVCXGREtwMhEyAHSJ1aqp` malgré son REJECT documenté :

1. Soumission du wallet parent → REJECT Fproject
2. Soumission des CA enfants un par un → NO GO maintenu
3. **Reformulation via changement de TP : 35% → 80%**

C'est le pattern exact de `erreur-001` (3 configs TP sur le même rugger : 150% / 100% / 70%).

## 🔍 Cause racine

### Le calcul du TP 80% était juste

Sur mes 14 lignes : pertes réelles -41%, -82%, -80%, -55% (moyenne -64,5%).

| TP | EV / trade |
|----|-----------|
| 35% | +6,6% |
| **80%** | **+38,7%** |

Les gagnants font +120% à +900%. Couper à 35% jetait l'essentiel du move en gardant tout le downside. **Le raisonnement arithmétique était correct** — et l'estimation initiale de Claude (+3,6%) était fausse, basée sur une moyenne de pertes approximative.

### Mais trois choses cassent le chiffre

**1. Six des 14 lignes ne sont pas de ce dev.**

Fproject compte **8 tokens** pour ce creator. Confirmés : `EjURSLP2`, `861z1ND2`, `8KnVsnTD`, `J4WbWdjCF`, `DdQpT8dr`, `AKUfUgMi`, `4zWtTQG8`, `2dVtBBHD`.

Absents de sa liste : `8JA24MGv`, `7EHU2LBj`, `ECyDXm7M`, `BvRhUcJ2`, `AY57uZs9`, `7oxdVAw1`

Dont **`8JA24MGv` — 6 → 253, soit +4117%** : mon plus gros gagnant, celui qui porte l'essentiel de l'EV. Il peut venir du creator lié (1 sibling détecté) mais ce n'est pas vérifié.

**2. Ma colonne ATH mesure le gain du dev, pas le mien.** Cf. `erreur-003`, bug B.

**3. Monter le TP aggrave la variable non mesurée.** Un token passe beaucoup moins de temps au-dessus de +80% qu'au-dessus de +35%. J'augmente l'EV théorique en réduisant la probabilité de toucher la cible. On ne répare pas un problème d'exécution non mesuré en éloignant la cible.

### Le REJECT ne portait pas sur le TP

| Métrique Fproject | Valeur |
|-------------------|--------|
| dev_score | **24 / 100** |
| Tokens dev-dumpés | **7 sur 8** |
| Flags | « Dev dumped after launch », « Dev sold 100% » |
| Taux de graduation | 12,5% (1/8) |
| Rug events | 6 |
| Âge wallet | 196 j |

Ce dev vend 100% de son bag après lancement, 7 fois sur 8. **Aucune valeur de TP ne change ça.** Le TP décide où je sors *si* je sors ; le dev décide *quand* le sol disparaît.

## 💸 Impact PnL

- **Montant perdu** : $0 (aucun trade exécuté)
- **Trades affectés** : 0
- **Coût réel** : temps de session × 3 reformulations

## ✅ Correction appliquée

1. NO GO maintenu sur `FAX4qRQd…`
2. **Règle** : un REJECT porte sur le wallet, pas sur la config. Changer le TP ne ré-ouvre pas un dossier fermé.
3. Si un setup rejeté est re-soumis → citer le précédent vault avant toute nouvelle analyse

### Ce qui rendrait ce dev ré-examinable

- [ ] Vérifier l'attribution des 6 CA orphelins
- [ ] Remesurer les 8 confirmés en gain depuis **mon entrée réelle**
- [ ] Si EV tient à +40% sur chiffres propres → créer une v1 en paper

## 🔒 Vérification

- [x] NO GO maintenu
- [ ] Nouvelle règle ajoutée dans `REGLES-OR.md`
- [x] `erreurs-recurrentes.md` mis à jour
- [x] `SCHEMAS-RUGGERS.md` mis à jour

## 📎 Liens

- Erreur mère : `06-ERREURS/erreur-001.md`
- Erreur liée : `06-ERREURS/erreur-003.md`
- Ruggers : `02-RUGGERS/SCHEMAS-RUGGERS.md`
