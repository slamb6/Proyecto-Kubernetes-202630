# Proyecto Kubernetes 202630 — Jobs parametrizados desde línea de comandos

## Integrantes

- Santy Baza Pérez
- Juan Benavides Barros
- Samuel Lambertino Gutiérrez

## Implementación

Se rellenaron los vacíos en `entrega/gestor_jobs.py` a partir de los comentarios
presentes en el la plantilla y la documentación de las api [core](https://github.com/kubernetes-client/python/blob/master/kubernetes/docs/CoreV1Api.md)
y [batch](https://github.com/kubernetes-client/python/blob/master/kubernetes/docs/BatchV1Api.md) 
v1 de kubernetes, así como sus clases relacionadas.

Como tarea adicional se añadió `indice` en python, que genera una lista de elementos
aleatorios, selecciona uno al azar y busca su índice, con los siguientes tamaños
según la complejidad:

|tarea|baja|media|alta|
|---|---|---|---|
|`indice`|250000|500000|1000000|

Para ello se actualizaron el diccionario del archivo fuente de python, el catálogo
y el diccionario `TAMANOS` del gestor de jobs.

## Demostración

[Video en youtube](https://youtu.be/5VDsKdek_XI)

## Otros

- Para descargar las dependencias del cliente de python de kubernetes mediante pip se
necesita Visual Studio Build Tools.
- Minikube debe iniciarse con `--container-runtime=docker` para poder vincular su
docker daemon a la terminal y construir las imágenes. Puede ser útil borrar el
caché de Minikube y borrar todo para hacer el cambio:
```powershell
minikube delete --all --purge
```
