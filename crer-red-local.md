
# Crear Red Local
---


### `2. Crear Red`

```bash
docker network create red-web
```

### `3. Añadir Contenedored a Red `

```bash
#listar container
docker ps
```

```bash
#Añadir Container GLPI
 docker network connect red-web <ID_CONTAINER_GLPI>
```

```bash
#Añadir Container NPM
 docker network connect red-web <ID_CONTAINER_GLPI>
```
