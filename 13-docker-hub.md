# 13 - Docker Hub

## ¿Qué es?

Docker Hub es un repositorio de imágenes donde puedes buscar, descargar y publicar imágenes Docker. [web:13][web:17]

## Para qué sirve

- Descargar imágenes oficiales como `nginx`, `mysql` o `ubuntu`.
- Subir tus propias imágenes para reutilizarlas en otros equipos o proyectos.
- Compartir versiones concretas de una app.

## Flujo básico

```bash
docker login
docker tag sitioweb:latest tuusuario/sitioweb:latest
docker push tuusuario/sitioweb:latest
```

## Qué debes entender

- `tag`: cambia el nombre de la imagen para que apunte a tu cuenta.
- `push`: sube la imagen al registro remoto.
- Luego esa imagen se puede descargar desde otra máquina con `docker pull`.

## Importancia real

Docker Hub es útil porque convierte tu imagen en algo portable y compartible, no solo local.
