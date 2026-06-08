
# 03 - Comandos básicos de Docker

## Imágenes

```bash
docker images
docker images --filter reference='*1.0'
docker images --no-trunc
docker rmi -f <id>
docker rmi nombre:tag
```

- `docker images`: muestra las imágenes locales. [web:8]
- `--filter reference='*1.0'`: filtra por nombre o tag.
- `--no-trunc`: muestra IDs completos para evitar ambigüedad.
- `docker rmi`: elimina imágenes que ya no necesitas.

## Contenedores

```bash
docker ps
docker ps --size
docker stop <id>
docker rm <id>
```

- `docker ps`: lista contenedores en ejecución. [web:8]
- `--size`: ayuda a ver cuánto ocupa el contenedor.
- `docker stop`: detiene el proceso principal.
- `docker rm`: borra el contenedor detenido.

## Construcción y ejecución

```bash
docker build -t sitioweb:latest .
docker run -it --rm -d -p 8080:80 --name web sitioweb
```

- `docker build`: construye una imagen desde un Dockerfile. [web:17]
- `-t`: etiqueta el nombre y versión.
- `.`: Docker usa el directorio actual como contexto.
- `docker run`: crea y arranca un contenedor a partir de una imagen.

## Qué hace cada bandera

- `-it`: útil para interacción y depuración.
- `--rm`: elimina el contenedor al salir, evitando basura.
- `-d`: lo deja corriendo en segundo plano.
- `-p 8080:80`: expone el puerto del contenedor al host.
- `--name`: da un nombre legible al contenedor.

## Qué debes entender de verdad

No memorices solo comandos: entiende el flujo. Primero construyes imagen, luego creas contenedor, luego inspeccionas, detienes y limpias. Si entiendes ese ciclo, ya puedes moverte en casi cualquier proyecto Docker.
