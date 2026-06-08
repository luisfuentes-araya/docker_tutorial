# 08 - EXPOSE

## ¿Qué hace?

`EXPOSE` indica qué puerto escucha la aplicación dentro del contenedor. Es una forma de documentar la intención del servicio, pero no publica el puerto por sí solo. [web:27][web:33]

## Ejemplo

```Dockerfile
FROM nginx:latest
EXPOSE 80
```

## Qué debes entender

- `EXPOSE 80` significa: “esta aplicación trabaja en el puerto 80 dentro del contenedor”.
- No abre el puerto hacia tu máquina automáticamente.
- Para publicar el puerto de verdad, se usa `-p` en `docker run`. [web:27][web:33]

## Ejemplo de publicación

```bash
docker run -d -p 8080:80 nginx
```

Aquí `8080` es el puerto del host y `80` el puerto del contenedor. Docker hace el mapeo para que puedas entrar desde tu navegador. [web:33]

## Uso real

`EXPOSE` sirve mucho para dejar claro en el Dockerfile qué puerto espera la aplicación. Es útil para documentación, para Compose y para mantener orden en proyectos donde varias personas trabajan sobre la misma imagen. [web:30][web:33]
