# Acceder contenedor

```bash
  docker ps
  docker exec -it <ID_CONTAINER> bash
```

# Despliege Producción

```bash
docker compose up -d --build

#Ignorar Cache(Solo si es necesario)
docker compose up -d --build --no-cache
```

# Despliegue Modo Local

```bash
docker compose up

# Si necesitas eliminar contenedor y volver desplegar
docker compose down -v
docker compose up
```
