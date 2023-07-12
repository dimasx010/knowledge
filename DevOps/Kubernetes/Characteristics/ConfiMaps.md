# Kubernetes ConfigMaps

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/cebf4929-e512-456f-9fca-de80a7a1bdc8">
</p>

Un ConfigMap es un diccionario de ajustes de configuración. Este diccionario consta de pares de cadenas clave-valor. Kubernetes proporciona estos valores a sus contenedores. Al igual que con otros diccionarios (mapas, hashes, ...), la clave le permite obtener y establecer el valor de configuración.

## ¿Por qué usaría un ConfigMap en Kubernetes?

Use un ConfigMap para mantener el código de su aplicación separado de su configuración.

Es una parte importante de la creación de una aplicación de doce factores.

Esto le permite cambiar fácilmente la configuración según el entorno (desarrollo, producción, prueba) y cambiar dinámicamente la configuración en tiempo de ejecución.

## ¿Para qué se utiliza un ConfigMap?

Un ConfigMap almacena ajustes de configuración para su código. Almacene cadenas de conexión, credenciales públicas, nombres de host y URL en su ConfigMap.

## Referencias
- https://matthewpalmer.net/kubernetes-app-developer/articles/ultimate-configmap-guide-kubernetes.html#:~:text=A%20ConfigMap%20is%20a%20dictionary,and%20set%20the%20configuration%20value.