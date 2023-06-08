# Clusters

## General

Un cluster de Kubernetes es un grupo de nodos (máquinas que ejecutan aplicaciones). Cada nodo puede ser una máquina física o una máquina virtual. La capacidad del nodo (su número de CPU y la cantidad de memoria) se define al crear el nodo. Un cluster comprende:

Al crear un nuevo clúster con Motor de contenedor para Kubernetes, especifique el tipo de clúster que desea crear. Puede especificar:

### Cluster mejorado

Los clusters mejorados soportan todas las funciones disponibles, incluidas las funciones no soportadas por los clusters básicos (como nodos virtuales, gestión de complementos de cluster, identidad de carga de trabajo y nodos de trabajador adicionales por cluster). Los clusters mejorados vienen con un acuerdo de nivel de servicio (SLA) con respaldo financiero.

### Cluster Basico

Los clusters básicos soportan todas las funciones principales proporcionadas por Kubernetes y Container Engine for Kubernetes, pero ninguna de las funciones mejoradas que proporciona Container Engine for Kubernetes. Los clusters básicos incluyen un objetivo de nivel de servicio (SLO), pero no un acuerdo de nivel de servicio (SLA) con respaldo financiero.

Tenga en cuenta lo siguiente al crear clusters:

Al utilizar la consola para crear un cluster, si no selecciona ninguna función mejorada durante la creación del cluster, tiene la opción de crear el nuevo cluster como un clúster básico. Por defecto, se crea un nuevo clúster como clúster mejorado, a menos que decida crear explícitamente un clúster básico.

Al utilizar la CLI o la API para crear un cluster, puede especificar si desea crear un clúster básico o un cluster mejorado. Si no especifica explícitamente el tipo de cluster que se va a crear, se crea un nuevo clúster como clúster básico por defecto.

En la siguiente imagen podremos analizar gráfica lo que serían los clústers

![image](https://github.com/dimasx010/knowledge/assets/105082657/e59fe88d-412f-468c-af99-7fe98e116cf0)

## Referencias
- https://docs.oracle.com/es-ww/iaas/Content/ContEng/Concepts/contengclustersnodes.htm#:~:text=Engine%20for%20Kubernetes.-,Clusters%20de%20Kubernetes,define%20al%20crear%20el%20nodo.