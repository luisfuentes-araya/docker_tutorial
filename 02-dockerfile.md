
# 02 - Dockerfile

## Qué es un Dockerfile

Un Dockerfile es un archivo de texto con instrucciones para construir una imagen paso a paso. [web:15]  
No es un contenedor ni una imagen: es la receta que Docker lee para crearla.

## Ejemplo base

```Dockerfile
FROM nginx:latest
COPY ./sitio /usr/share/nginx/html
```

## Explicación profunda

- `FROM nginx:latest`  
  Define la imagen base. Docker descargará esa imagen si no la tiene localmente. Elegir una base concreta importa, porque la base define el sistema, herramientas y seguridad de partida. [web:15]

- `COPY ./sitio /usr/share/nginx/html`  
  Copia archivos desde tu proyecto local a la ruta interna del contenedor. Esa ruta es importante porque Nginx sirve contenido web desde ahí por defecto. [web:18]

## Qué significa construir una imagen

Cuando haces `docker build`, Docker lee el Dockerfile, ejecuta cada instrucción y guarda el resultado en capas. Si vuelves a construir sin cambios, Docker reutiliza capas anteriores para acelerar el proceso. [web:15]

## Buenas prácticas

- Usa una imagen base específica si quieres más control que `latest`.
- Reduce archivos innecesarios con `.dockerignore`.
- Ordena el Dockerfile desde cambios menos frecuentes a más frecuentes para aprovechar el cache.
- Evita meter credenciales o secretos dentro de la imagen.

## Ejemplo con tu caso

Si tu repo tiene un sitio web de clientes, el Dockerfile puede servir esa carpeta desde Nginx, y tú solo cambias los archivos HTML sin rehacer toda la lógica del despliegue. [image:20]
