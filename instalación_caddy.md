# Instalación Caddy Ubuntu 22
---

### `1. Clonar Repositorio`

```bash
sudo apt install -y curl apt-transport-https gnupg lsb-release debian-keyring debian-archive-keyring

curl -1sLf 'https://dl.cloudsmith.io/public/caddy/stable/gpg.key' \
  | sudo gpg --dearmor -o /usr/share/keyrings/caddy-stable.gpg

echo "deb [signed-by=/usr/share/keyrings/caddy-stable.gpg] \
https://dl.cloudsmith.io/public/caddy/stable/deb/ubuntu $(lsb_release -cs) main" \
  | sudo tee /etc/apt/sources.list.d/caddy-stable.list

```
