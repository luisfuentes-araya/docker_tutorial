# 12 - Redes de Docker

## ¿Qué son?

Las redes permiten que contenedores se comuniquen entre sí de forma controlada. [web:17]

## Tipos comunes

- `bridge`: red privada por defecto para contenedores en una misma máquina.
- `host`: comparte la red del host.
- `none`: sin red.
- Redes creadas por el usuario: recomendadas para proyectos organizados. [web:17]

## Comandos básicos

```bash
docker network ls
docker network create mi_red
docker network inspect mi_red
```

## Idea clave

Si tienes frontend, backend y base de datos, la red de Docker permite que se vean por nombre de servicio sin depender de IPs manuales.

## Relación con Compose

Compose normalmente crea una red propia para los servicios del proyecto, lo que hace más fácil que los contenedores se encuentren entre sí.
