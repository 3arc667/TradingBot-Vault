# 🔒 SÉCURITÉ — Informations sensibles

> ⚠️ **CE FICHIER NE DOIT JAMAIS CONTENIR DE VRAIES CLÉS**
> Utilise uniquement des références et des emplacements

---

## 🔑 Clés et accès

| Type | Emplacement réel | Notes |
|------|-----------------|-------|
| Clé API Fproject | Variables d'environnement Windows | `FPROJECT_API_KEY` |
| Clé privée wallet | Wallet physique / Ledger | Jamais sur PC |
| RPC Solana | Fichier `.env` du bot | Dans dossier bot, PAS ici |
| Telegram Bot Token | Variables d'environnement | `TELEGRAM_BOT_TOKEN` |

## 🛡️ Bonnes pratiques

- [ ] 2FA activé sur tous les comptes
- [ ] Wallet principal = cold storage
- [ ] Wallet trading = montant limité
- [ ] Backup des clés sur papier (pas cloud)
