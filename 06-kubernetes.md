
# 06 - Kubernetes

## Qué es Kubernetes

Kubernetes es una plataforma de orquestación de contenedores. Su trabajo es decidir dónde correrlos, cuántas copias mantener y qué hacer si uno falla. [web:16][web:19]

## Relación con Docker

Docker crea y ejecuta contenedores. Kubernetes coordina muchos contenedores en varios nodos.  
En simple: Docker resuelve el contenedor; Kubernetes resuelve la operación a escala.

## Conceptos clave

- **Pod**: unidad mínima de ejecución en Kubernetes. [web:19]
- **Deployment**: define réplicas, actualizaciones y estado deseado.
- **Service**: expone pods y estabiliza el acceso.
- **Cluster**: conjunto de máquinas donde corre Kubernetes.

## Por qué importa

Si una app crece, ya no basta con un `docker run`. Necesitas alta disponibilidad, escalamiento y recuperación automática. Ahí Kubernetes tiene sentido. [web:16][web:19]

## Cómo verlo en tu cabeza

Docker es como tener un contenedor de clientes funcionando en una sola máquina. Kubernetes es como tener muchos de esos contenedores distribuidos, balanceados y vigilados por un sistema que los mantiene vivos.
