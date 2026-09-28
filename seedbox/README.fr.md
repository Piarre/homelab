# Seedbox

[English](README.md)

qBittorrent derrière un VPN Mullvad (WireGuard) avec Gluetun.

## Utilisation

```bash
cp .env.example .env   # puis remplir .env
docker compose up -d
```

Interface web : `http://<ip>:8080`

Le mot de passe admin temporaire est dans les logs : `docker logs qbittorrent`

## Variables d'environnement

| Variable | Description | Exemple |
|---|---|---|
| `MULLVAD_PRIVATE_KEY` | Clé privée WireGuard (depuis Mullvad) | |
| `MULLVAD_ADDRESS` | Adresse WireGuard (depuis Mullvad) | `10.x.x.x/32` |
| `VPN_PROVIDER` | Fournisseur VPN | `mullvad` |
| `VPN_TYPE` | Protocole VPN | `wireguard` |
| `VPN_SERVER_COUNTRIES` | Pays du serveur VPN | `Netherlands` |
| `TZ` | Fuseau horaire | `Europe/Paris` |
| `OUTPUT_FOLDER` | Dossier de téléchargement sur l'hôte | `/path/to/downloads` |

## Ports

| Port | Service |
|---|---|
| `8080` | Interface web qBittorrent |
