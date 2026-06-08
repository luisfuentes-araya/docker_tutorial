# 10 - CMD

## ¿Qué hace?

`CMD` define el comando por defecto o los argumentos por defecto que se ejecutan cuando arranca el contenedor. [web:28][web:31]

## Ejemplo

```Dockerfile
FROM nginx:latest
CMD ["nginx", "-g", "daemon off;"]
```

## Qué significa

- Si no defines nada más, el contenedor usará ese comando al iniciar.
- Si luego pasas otro comando al ejecutar `docker run`, puedes reemplazar ese comportamiento. [web:28][web:34]

## Relación con ENTRYPOINT

- `CMD` da flexibilidad.
- `ENTRYPOINT` fija el comportamiento principal. [web:28][web:31]

## Regla mental

Usa `CMD` cuando quieras un valor por defecto que se pueda cambiar fácil en runtime. Si tu contenedor tiene una tarea principal que no debería variar, entonces `ENTRYPOINT` suele tener más sentido. [web:31][web:34]
