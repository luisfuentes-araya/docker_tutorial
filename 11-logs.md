# 11 - Logs y depuración

## ¿Para qué sirven?

Los logs te permiten ver qué está haciendo el contenedor por dentro: errores, arranque de la app, peticiones, fallos de configuración y mensajes del servidor. [web:17]

## Comandos útiles

```bash
docker logs <id>
docker logs -f <id>
docker inspect <id>
docker exec -it <id> bash
```

## Explicación

- `docker logs <id>`: muestra la salida del contenedor.
- `-f`: sigue los logs en tiempo real.
- `docker inspect`: entrega información detallada sobre red, mounts, variables y configuración.
- `docker exec -it`: entra al contenedor para revisar archivos o probar comandos.

## Buen criterio

Cuando algo falla, no adivines: mira primero logs, luego inspect, y si hace falta entra al contenedor para verificar qué existe realmente.
