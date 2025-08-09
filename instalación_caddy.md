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


### `2. Actualizar e Instalar`

```bash
sudo apt update
sudo apt install -y caddy
```


### `3. Activar y arrancar Caddy`

```bash
sudo systemctl enable caddy
sudo systemctl start caddy
```

### `3. Configurar Dominio`

```bash
#Editar Archivo:
sudo nano /etc/caddy/Caddyfile
```
```bash
#Agregar Configuración al archivo
dirislimaeste.xyz {
    reverse_proxy 127.0.0.1:8080
}
```




