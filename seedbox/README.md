# Seedbox

[Français](README.fr.md)

qBittorrent behind a Mullvad VPN (WireGuard) with Gluetun.

## Usage

```bash
cp .env.example .env   # then fill in .env
docker compose up -d
```

Web UI: `http://<ip>:8080`

The temporary admin password is in the logs: `docker logs qbittorrent`

## Environment variables

| Variable | Description | Example |
|---|---|---|
| `MULLVAD_PRIVATE_KEY` | WireGuard private key (from Mullvad) | |
| `MULLVAD_ADDRESS` | WireGuard address (from Mullvad) | `10.x.x.x/32` |
| `VPN_PROVIDER` | VPN provider | `mullvad` |
| `VPN_TYPE` | VPN protocol | `wireguard` |
| `VPN_SERVER_COUNTRIES` | VPN server country | `Netherlands` |
| `TZ` | Time zone | `Europe/Paris` |
| `OUTPUT_FOLDER` | Download folder on the host | `/path/to/downloads` |

## Ports

| Port | Service |
|---|---|
| `8080` | qBittorrent web UI |
