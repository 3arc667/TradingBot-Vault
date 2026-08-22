---
date: 2026-08-22
type: analyse-reseau
statut: 🔴 ACTIF — infrastructure confirmée, analyse complète
titre: Hub 5ARipQXUFP13 — Analyse complète Type A/B/C (pages 1+2)
version: 2
---

# Hub 5ARipQXUFP13 — Infrastructure de financement
## 400 enfants analysés (pages 1+2 de N)

---

## Nœuds du réseau

| Rôle | Adresse | Notes |
|------|---------|-------|
| **Hub central** | `5ARipQXUFP13QzHau8moMxpvLzXwMLgLgpzjpbsrUzTa` | Labellisé "hub" par Fproject. Actif depuis ~6 mois. Volume total: dizaines de milliers de SOL |
| **Atomic relay (Binance→hub)** | `EDjdKegL317Fq543eLEvUKXQoNr5MHbZrzXgLVqy1jU3` | 140 SOL depuis Binance HW2, 23x vers AKbotZVF (gas). Forward: `8bxL7nRuiWFTGm52GX6BTvEY3ntQamcz3EuTLbt8TfjB` |
| **Gas distributor** | `AKbotZVF3zr9i4Cz2Lv34s6SydytjdidruoGTnvwPxFh` | Petits montants depuis EDjdKegL — rôle: gas/déploiement devs |
| **Nœud circulaire** | `wae8YMC7PWjcPbM3mdx3CUDZEkkjaFAE4VxS5mF2YuN` | Boucle bidirectionnelle confirmée avec 5ARip (envoie ET reçoit). `unresolved_forward` |
| **Hub secondaire** | `7cNrAnWGxFouM523ewCnYbp2EyU2FaBnbSYxYTE9973D` | 1546 SOL depuis 5ARip (3 virements) — labellisé "hub" |
| **Hub tertiaire** | `6vJEkT5hfgz4bzauQJvUwnMy7zKRYAE5fDHm7xeN44nz` | 747 SOL depuis 5ARip — labellisé "hub" |
| **Hub quaternaire** | `BvD8pk9XMTYJrcjruFwrLCmM6pf5HshyXPSFAeYqkRUv` | 659 SOL depuis 5ARip — labellisé "hub" |
| **Nœud relais** | `2u2tU5RgCBdphiRFpMWYtYBtnmvz2aG7QJ93U4C8NfdD` | 2629 SOL, 608 virements depuis 5ARip — très actif, probablement relay ou exchange interne |

## Exchanges dans la chaîne
| Exchange | Adresse Hot Wallet |
|----------|--------------------|
| Binance Hot Wallet 2 | `5tzFkiKscXHK5ZXCGbXZxdw7gTjjD1mBwuoFbhUvuAi9` |
| Bitgate Hot Wallet | `EL8bhbm1C2ifh8xagRy51tasSgj2umefj1vM8ThLS8Kv` |
| Bitget Hot Wallet | `A77HErqtfN1hLLpvZ9pCtu66FEtM8BveoaKbbMoZ4RiR` |
| OKX | `is6MTRHEgyFLNTfYcuV4QBWLjrZBfmhVNYR6ccgr8KV` |
| Bybit Hot Wallet 10 | `iGdFcQoyR2MwbXMHQskhmNsqddZ6rinsipHc4TNSdwu` |
| Kraken Hot Wallet 1 | `6LY1JzAFVZsP2a2xKrtU6znQMQ5h4i7tocWdgrkZzkzF` |
| Gate Hot Wallet | `u6PJ8DtQuPFnfmwHbGFULQ4u4EgjDiyYKjVEsynXq2w` |

---

## TYPE A — Signal dev exploitable ✅

### Définition
- 1 virement unique depuis 5ARip
- Montant **570–1230 SOL avec décimales significatives** (ex: 863.732..., 787.xxx...)
- Wallet jamais actif avant ce virement
- Note technique: chaque entrée apparaît deux fois (source `sol` + source `helius`) = même wallet, doublon à filtrer

### Distribution des montants (400 enfants analysés)
| Plage | Volume | Signification |
|-------|--------|---------------|
| 1000–1230 SOL | ~12 wallets | Devs "premium", gros capital |
| 850–999 SOL | ~40 wallets | Cœur du pattern, les plus fréquents |
| 700–849 SOL | ~50 wallets | Profil dev solide |
| 570–699 SOL | ~60 wallets | Base du profil |

### Rythme: ~3–6 nouveaux wallets Type A par jour. Hub continu, pas sporadique.

### Wallets Type A les plus récents (HOT — priorité de qualification)
| Wallet | SOL | Timestamp |
|--------|-----|-----------|
| `9KvN1Fg2NH7Ay9XJ8f2RNy3SqZMchUG494NQL4LMeqYF` | 1230 | 2026-08-22 (très récent) |
| `57SXT8scxT1J1my4mgRdoxqtSy4quG1Bi67oicLpwX8J` | 850 | 2026-08-22 (très récent) |
| `3xnfLQkRfGpXqbA2hbghdqhH7Q8hGZUvTpntggAM2WD5` | 787 | 2026-08-22 (très récent) |
| `FL15v3sYDFhn6WPy1jMXgRoptzmJ2uMtArjwouZ9UuLg` | 260 | 2026-08-22 (Type C — à noter) |
| `84gJ17ZWZ6QEUtKzutjBomR4YbbeZKEDU11dr7gTMf1q` | 80 | 2026-08-22 |
| `BqF5Bd8QMoruxyDhC6DNHixwRR9J1A2EotW5Md6GxZxp` | 787 | récent |
| `39SEyTg2Du3BncG5mcGixAShBNFGZLHcfumZyoFyszi2` | 897 | récent |
| `5PmUagibJGrAgvzcqm2cVDg6rcAKFrPimuYPpkv2HG3i` | 857 | récent |
| `BZmjdZeWzhEt4qfVhYW5R8RqPkbc61p84io4pHvkuPmd` | 904 | récent |
| `6eBHQqdtE3WSYCbstJq1NM9b5EVQ3z7kU99nuu2mgNaa` | 823 | récent |
| `E1NhKkN2pmzFpLy3C1FjHDwTvFFtyYHaVyqgU5Widqnx` | 1018 | récent |
| `7jXwyPpfGcdXF7uCammLutTNrVLhXjoqyn6q5hLE9Brn` | 900 | récent |
| `GG7xP6UJgQMvraNMB4XUJUx5YCGMMTEe9N6JtqqaVzs9` | 900 | récent |
| `8nijx7pq4RVtXpEvHMJq3a47EWd4bwExQLLf5LE4nd9F` | 935 | récent |
| `DZeCk8cMgpgMx9LkWXFFMcYhUmnm6DmozZAXyMTGpV6W` | 863 | récent |
| `G7JtA44USX6qhWh4iaMLmZLY1UzmbbbaejHWjpK6syCy` | 727 | récent |
| `7L2NVertJfjT8VhUUhhBoEngyVxTbGGjqPVEeR5hAWr4` | 838 | récent |
| `ASjrXN1uKEqSCswMBkAHbHWKc1dK3YxizG6c66vPaN44` | 838 | récent |
| `3htRKVYyQUbJahWSP7BJ3wvLfyuh8RtToEQFZwUNmTSg` | 738 | récent |
| `DFsAw7PqZhM79YSPsXRDZw2HL1vZxZUXgsgca2KK3Meo` | 860 | récent |
| `FNAVZuDVzryGzugvKnXohURjamVxcAZM3NNngKsHNR5x` | 845 | récent |
| `EqnzE4iBNVcBwdRhk2tJJTeMzsF3zjjFT8TvmWYTg9ZG` | 852 | récent |
| `Eiedwqqknr2qe36P6WjGGCdWd2FHaFb6PLUCfp8deYUH` | 902 | récent |
| `GigfBKsrR5a8X1sQo3yTrQuPUQLCHRY5PPvnpnCtqocD` | 861 | récent |
| `DFvm3zk8jmNZZaRT3d4Gp4gQWKiCaNPqen14wT1323SE` | 735 | récent |
| `EJqNeUQ5L7AwXXsNrhPBM8fABW5XLhCzThdbemPMhKGn` | 800 | récent |
| `3bzCkzwrqgVq93xXv1HrQ8mNZGw48XC7kEaN5KCjvmVL` | 800 | récent |
| `BjYj7cC8svBN7Unqsu6rPP6Tcfmar2WsQHGtS2W5jn8p` | 944 | récent |
| `HvymaShwnALwGyCKA4aKocYkBijMeTfYzjeE52N1cqEf` | 941 | récent |
| `2vyXVyDaYQKdDWj4SUzMxMzPqbMa2yqtfPYiLfSC3bWh` | 864 | récent |
| `Ap7TdZuKwhqdfqaybGEhX9KnwymiKQbDQFiy293tTggb` | 792 | récent |
| `3Cg3ZE5A4PzA5tdyKfFiu3daSnWkiWFrwfQFZmJsRgnr` | 772 | récent |
| `9m5KezFkHTtqzD9ZyCNdakLJ66ETdG6Cf3dB5UyoD1NC` | 755 | récent |
| `F8FfihMoJJyMSj2GhN7CR14WGYB8fA9E9qY1BnA6zPBw` | 947 | récent |
| `149MJesC5XKqbyybqmkRKJjhsUjgLGoP3vUuYa7Y36F` | 892 | récent |
| `7btsmh97svbxBKTAGf3fQBJ7Ry2f5ASZ3YV9UViKx6hi` | 903 | récent |
| `CDGaHf6PMxJsq4wsPrdEuNxeVokkbrnCkKqhXjFsZNJ` | 927 | récent |
| `7j5WGbBSJbEKAMNkQXhiTXETBLFDKuwqFtkpAX1jHpn4` | 838 | récent |
| `FsJjwuUueWS2g4g7xGhBjgbdkLVZ4rJMd1uHEH3L1UN9` | 745 | récent |
| `AsM84HKLXsvyv9SA3jmFQsa7dHuJLJEnpcZ1jURtB7Ca` | 748 | récent |
| `7Z48NVUaYVA1FAiCMNZeheUc6Y82vZAqFF9fKPeAY6qM` | 679 | récent |
| `FRp3zkAaqb5XV5vR9Jjz6GW2Yg2gpiDVUpRVVjouc7BK` | 573 | récent |
| `2yBc99AUVJEnHVKqCHdMcRC7xXAc1N7raDX8WMmjVqfH` | 526 | (limite basse) |
| `GJ2yGNaDhKVRu2Vjeo5fJ7PEh2DhGSpFcX9vx9wkYo7i` | 621 | récent |
| `GYH5yB9Ck7NKbBw4M7rsw6HcqE7PresPkuTu5nPQoA2` | 698 | récent |
| `BdTdUQDScyTEuRXiiJLjHFzzyX6hpLRhWANSHemMeUnj` | 672 | récent |
| `8huo31ATuFT98cLufCNKpKHtMgTCwnTjCvtBhxPXqF8Q` | 656 | récent |
| `DqMhM1tPUAa6VvxVdrYEUp3GZrn4TcG7KScMuUKHGJds` | 639 | récent |
| `14qiATU7JdnCz9McC2gKGxBr95Tr2xVXkqFfsQFX3VAR` | 614 | récent |
| `EcAnQ4e7jSFuL52ZjU2KbNh7BkMvwqL76aUcDQamuTEi` | 650 | récent |
| `CJH26Dmc98XFNwcEXyzN552fqQTXUY5ynhQcsQgT7WTt` | 582 | récent |
| `EabW64v8ys6TsBV4MqnNiqEUizsje8vHzY1P6ca34BKe` | 592 | récent |
| `8RqqAA1GnxdMxEa6uqDkmjLdgBUMMTqDE2fjzfQV6FCk` | 820 | récent |
| `B1WX9WYTxnc8rkVUp3D4WVWsteCNizKqShd9W7Vr2UWB` | 820 | récent |
| `633CS5ghYNT7bYARjibFsvuMCTZuoK8bqpiNvZBghtkc` | 962 | récent |

---

## TYPE B — Blocs 365 SOL (infrastructure interne) ⚠️

### 9 wallets identifiés
```
JDqFtYYG1nhZ1Jonk9Z8WnAimWWe25z2uWRXhnBBh4xN
EQiaxogvgRcUo8UeRBPq393jk3MTtuHrxg9HLPcYpPbW
CYkvor321X35ygmfciXyHNPHb1q7JiRu1dPDmR5NV7dV
EP6jniTw8gufE4NChZN1kzHY5qDeDN3pwZx6zSWBxzTg
BK8rJ73NxQejq29JhYEB7L4TmM4fKEAqjPf11RsgxeQm
9NGXX7s1tTC4rNrw5NNL3hdKJLkGAQH12iM4pRUW524s
5mLQQ9i2m8oi3UFTMh9UPZUnr58gP2pcVHgF47K5cLdf
3EkfjxMc4E7vsbWhCfcX4mEPgKBPs8YLZc5MNjHYnzLV
EWsg7FrFATwkvnyDNvzo8nDDJdCYFnF8FyLeVKx9943B
```

### Interprétation
- Groupe **fini** (pas de nouveau 365 SOL en page 2)
- Montant rond trop précis pour du capital de lancement
- Probablement: sous-relais, tranche opérationnelle, comptes de réserve de l'infrastructure
- **Ne pas snipper ces wallets** — ne sont pas des devs, probablement des bras d'un sous-réseau distinct
- Valeur: cartographier leurs sorties pour comprendre la topologie

---

## TYPE C — Petits montants ronds (gas / réappro) ❌ pas de snipe

### Signatures observées
- **0.1 SOL × 5 en rafale** = gas pur (frais de déploiement, création de comptes)
- **20–150 SOL ronds** = réapprovisionnement de comptes opérationnels intermédiaires
- **200–500 SOL ronds** = probablement réappros de sous-relais ou comptes de rotation

### Règle de filtrage
> Si le montant est un entier ou se termine par .000 ou .9999, c'est Type C — skip.
> Si le montant a des décimales significatives (ex: 863.732634865) et est entre 570–1230 SOL, c'est Type A — qualifier.

---

## Règle d'exploitation (synthèse)

**Trigger de snipe potentiel:**
1. Nouveau wallet reçoit **570–1230 SOL depuis 5ARipQXUFP13**
2. Montant avec décimales (Type A confirmé)
3. Wallet sans historique de launch

**Action:** → qualifier via `fproject_rugger_cex_research` ou `fproject_token_analysis` sur les premiers tokens créés → si dev rug >80%, envisager copytrade

**NE PAS tracker:** wae8YMC (boucle), AKbotZVF (gas), EDjdKegL (relay), wallets 365 SOL (Type B), petits montants ronds (Type C)

---

## Pagination
- Page 1: 200 enfants (22 août, ~18h → 18 août ~06h34)
- Page 2: 200 enfants (18 août ~06h34 → 15 août ~14h05)
- **next_cursor p3**: `2026-08-15T14:05:55.512585Z|BuyDH68YjCVSHK2istuR7pV7TvQrVcy8zkQibVtXLdea`
- Pages restantes: encore disponibles (hub actif depuis ~6+ mois)

## Items à faire
- [ ] Paginer page 3+ (next_cursor disponible)
- [ ] Qualifier top 5 wallets Type A les plus récents via fproject_token_analysis
- [ ] Investiguer les 9 wallets Type B — voir leurs sorties
- [ ] Vérifier CBmRi4nqviUZWt9v7jaB23BAaGqBG2XnCqvxnbbAz8eu (lien AKbotZVF → OKX)
- [ ] Résoudre fragments: `BLnA72XN7Jvt5oP…` et `4f5s927ybxjQc7Q…`
