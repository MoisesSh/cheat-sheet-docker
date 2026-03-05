# Cheat Sheet ![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)

## Verificacion de instalación y Estados Iniciales 

| Comando | Utilidad |
|----------|----------|
| `docker ---version` | Verificar instalacion y version de docker |
| `docker info` | Informacion del sistema |
|`docker images`| Listar imagenes locales |
|`docker ps`|Listar contenedores activos|
|`docker ps -a`|Listar contenedores (incluye detenidos)|
 
---

## Comandos de ciclo de vida de la aplicación 
| Comando | Utilidad |
|----------|----------|
|`docker ps`|Listar contenedores activos|
|`docker ps -a`|Listar contenedores (incluye detenidos)|
| `docker compose build` | Construir la imagen |
| `docker compose build <nombre_servicio>` | Construir imagen especifica |
| `docker compose up` | Corre la  en primer plano  |
|`docker compose up -d`| Corre la aplicación en segundo plano (silencio) |
|`docker compose up -d --build`| Construye y levanta los contenedores (silencio) |
|`docker compose down <nombre_servicio>`|Detenemos el servicio especifico|
|`docker compose down`|Detenemos todos los servicios|

---
## Comandos de administracion de imagenes y/o Contendores
| Comando | Utilidad |
|----------|----------|
|`docker rm <container_id>`|Elimina un contenedor usando su ID|
|`docker rmi <image_id>`|Elimina una imagen específica usando su ID o nombre|
|`docker system prune`|Borra basura técnica pero mantiene tu data y tus imágenes con nombre|
|`docker system prune -a`|Borra también las imágenes que no se están usando (aunque tengan nombre)|
|`docker system prune --volumes`|Borra los volúmenes que no estén en uso|



---
## Comandos para obtener la información de los servicios
| Comando | Utilidad |
|----------|----------|
|`docker-compose logs <nombre_servicio> `|Ver logs de servicio especifico|
|`docker-compose logs -f`|Ver logs en tiempo real|

---

![image](https://avatars.githubusercontent.com/u/5429470?s=200&v=4)
<br>
[Documentacion Oficial De Instalacion](https://docs.docker.com/desktop/setup/install/linux/debian/)
### Tip Extra
> Estos comandos nos permiten interactuar directamente con el contenedor
~~~
docker exec -it <nombre_servicio> /bin/bash 
docker exec -it <nombre_servicio> sh 
~~~
