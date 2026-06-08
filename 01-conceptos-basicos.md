# 01 - Conceptos básicos de Docker

## ¿Qué problema resuelve Docker?

Docker sirve para ejecutar aplicaciones de forma aislada y reproducible. [web:12]  
Antes, una app podía funcionar en tu PC y fallar en otra por diferencias en sistema operativo, librerías o versiones. Docker reduce ese problema empaquetando la app junto con su entorno. [web:5][web:14]

## Imagen, contenedor y capa

- **Imagen**: plantilla inmutable con instrucciones y sistema base para crear contenedores. [web:12]
- **Contenedor**: instancia viva de una imagen, con su propio proceso, red y sistema de archivos aislado. [web:17]
- **Capas**: cada instrucción del Dockerfile crea una capa reutilizable, lo que ayuda a construir imágenes más rápido cuando no cambian todas las partes. [web:15]

Una forma útil de pensarlo es esta: la imagen es el molde y el contenedor es la copia en ejecución.

## Qué pasa internamente

Cuando ejecutas un contenedor, Docker usa el kernel del host, pero aísla procesos, red y archivos para que la app se comporte como si estuviera sola. [web:14][web:17]  
Eso hace que Docker sea más liviano que una máquina virtual, porque no necesita simular un sistema operativo completo. [web:12]

## Ejemplo visual

En un proyecto como el tuyo, podrías imaginar una app web de clientes servida por Nginx dentro de un contenedor, mientras tu carpeta local mantiene los archivos HTML y datos de prueba. [image:20]

## Beneficios reales

- Portabilidad: la misma imagen corre igual en distintas máquinas. [web:5]
- Repetibilidad: lo que construyes hoy lo puedes volver a levantar mañana con el mismo resultado. [web:14]
- Aislamiento: puedes probar versiones sin dañar tu sistema principal.
- Velocidad: crear, borrar y recrear contenedores es más rápido que reinstalar software manualmente.
