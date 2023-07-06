# Amazon Elastic Container Registry ECR

Amazon Elastic Container Registry (Amazon ECR) es un servicio de registro de imágenes de contenedor administrado por AWS que es seguro, escalable y fiable. Amazon ECR admite repositorios privados con permisos basados en recursos mediante AWS IAM. De este modo, los usuarios especificados o las instancias de Amazon EC2 pueden acceder a sus repositorios e imágenes de contenedor. Puede utilizar la CLI preferida para insertar, extraer y administrar imágenes de Docker, imágenes de Open Container Initiative (OCI) y artefactos compatibles con OCI.

El equipo de servicios de contenedores de AWS mantiene una hoja de ruta pública en GitHub. Contiene información acerca del trabajo actual de los equipos y permite a todos los clientes de AWS dar retroalimentación de forma directa. Para obtener más información.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4a1c7e68-1b06-4bb8-8309-23da15c05317">
</p>

## Componentes de Amazon ECR

Amazon ECR contiene los siguientes componentes:

### Registry (Registro)
Cada cuenta de AWS recibe un registro privado de Amazon ECR; puede crear un repositorio o más en su registro y almacenar imágenes allí. Para obtener más información

### Token de autorización
Debe autenticar el cliente en los registros de Amazon ECR como usuario de AWS para que dicho cliente pueda insertar y extraer imágenes. 

### Repositorio
Un repositorio de Amazon ECR contiene las imágenes de Docker, las imágenes de Open Container Initiative (OCI) y artefactos compatibles con OCI. 

### Política sobre repositorios
Puede controlar el acceso a los repositorios y a las imágenes que contienen mediante políticas.

### Imagen
Puede insertar y extraer imágenes de contenedor en los repositorios y utilizarlas localmente en su sistema de desarrollo o en definiciones de tareas de Amazon ECS y especificaciones del pod de Amazon EKS

## Características de Amazon ECR

Amazon ECR ofrece las siguientes características:

Las políticas de ciclo de vida ayudan a administrar el ciclo de vida de las imágenes en sus repositorios. Debe definir reglas que den como resultado la limpieza de imágenes no utilizadas. Puede probar reglas antes de aplicarlas al repositorio

El escaneo de imágenes permite identificar vulnerabilidades de software en las imágenes de contenedor. Los repositorios se pueden configurar para escanear al insertar. Esto garantiza que cada nueva imagen insertada al repositorio se escanee. A continuación, puede recuperar los resultados del escaneo de la imagen.

La replicación entre regiones y entre cuentas hace que sea más fácil tener las imágenes donde las necesite. Se configura como un parámetro del Registro y se aplica por región.

Las reglas de almacenamiento en caché proporcionan una forma de almacenar repositorios de almacenamiento en caché en registros públicos remotos de su registro privado de Amazon ECR. Mediante una regla de caché de extracción, Amazon ECR se pondrá en contacto periódicamente con el registro remoto para asegurarse de que la imagen almacenada en caché de su registro privado de Amazon ECR esté actualizada

## Referencias
- https://docs.aws.amazon.com/es_es/AmazonECR/latest/userguide/what-is-ecr.html


