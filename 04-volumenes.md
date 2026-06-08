# 04 - Volúmenes

## Qué resuelve un volumen

Un volumen o montaje permite que los archivos vivan fuera del contenedor para no perderlos al borrar o recrear la instancia. [web:12]  
Eso es clave cuando cambias contenido web, bases de datos o archivos de trabajo y no quieres rehacer la imagen cada vez.

## Bind mount

```bash
docker run -it --rm -d -p 8080:80 \
  -v ./sitio:/usr/share/nginx/html \
  --name web sitioweb
```

- `./sitio`: carpeta de tu proyecto local.
- `/usr/share/nginx/html`: carpeta donde Nginx busca el contenido web. [web:18]
- Los cambios en tu editor se reflejan casi al instante en el navegador.

## Diferencia importante

- **Bind mount**: vincula una carpeta real del host.
- **Volumen administrado por Docker**: Docker guarda y gestiona los datos por su cuenta. [web:12]

## Cuándo usar cada uno

- Usa bind mounts para desarrollo y pruebas rápidas.
- Usa volúmenes administrados por Docker para persistencia más limpia en bases de datos o ambientes más controlados.

## Relación con tu ejemplo de clientes

En un proyecto de clientes, podrías montar una carpeta con archivos HTML de fichas, imágenes o reportes, y el contenedor solo se encarga de servirlos sin perder lo que editas. [image:20]
