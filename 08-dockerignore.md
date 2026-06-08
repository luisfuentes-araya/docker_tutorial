# 07 - .dockerignore

## ¿Qué es?

El archivo `.dockerignore` le dice a Docker qué archivos o carpetas **no** debe incluir en el contexto de build cuando construye una imagen. [web:26][web:29]

## ¿Por qué importa?

Cuando ejecutas `docker build`, Docker manda todos los archivos del directorio al motor de construcción. Si envías cosas innecesarias como logs, `.git`, archivos temporales, backups o dependencias pesadas, la imagen puede volverse más lenta de construir y más grande de lo necesario. [web:26][web:32]

## Ejemplo básico

```txt
.git
node_modules
*.log
README.md
.env
tmp/
```

## Explicación

- `.git`: evita enviar el historial del repositorio.
- `node_modules`: normalmente se reinstala dentro del contenedor si hace falta.
- `*.log`: evita archivos de registro temporales.
- `.env`: reduce el riesgo de copiar secretos por accidente.
- `tmp/`: carpetas temporales que no aportan al runtime. [web:26][web:29]

## Idea clave

`.dockerignore` no cambia la app; cambia lo que Docker recibe para construir la imagen. Eso ayuda a construir más rápido, gastar menos espacio y evitar errores por archivos que no deberían ir dentro del contenedor. [web:26][web:32]
