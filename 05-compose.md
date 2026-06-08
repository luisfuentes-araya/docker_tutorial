
# 05 - Docker Compose

## Para qué sirve

Docker Compose permite definir servicios completos en un archivo YAML y levantarlos con un solo comando. [web:7]  
Es útil cuando una app no es solo un contenedor, sino varios componentes que deben arrancar coordinados.

## Ejemplo simple

```yaml
version: "3.8"

services:
  web:
    image: sitioweb:latest
    ports:
      - "8080:80"
    volumes:
      - ./sitio:/usr/share/nginx/html
```

## Qué debes entender

- `services`: lista los componentes de tu aplicación.
- `image`: usa una imagen ya creada.
- `ports`: expone el servicio hacia fuera.
- `volumes`: monta archivos del host dentro del contenedor. [web:7]

## Flujo mental correcto

Compose no reemplaza Docker; lo organiza. Primero defines la imagen o servicio, luego levantas todo el entorno junto, y después puedes detenerlo sin manejar contenedor por contenedor.

## Cuándo vale la pena

Cuando tu proyecto crezca y tengas frontend, backend y base de datos, Compose te ahorra mucho trabajo manual.
