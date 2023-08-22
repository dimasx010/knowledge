# AWS Macie

Amazon Macie es un servicio de seguridad de datos que descubre datos confidenciales mediante el machine learning y la coincidencia de patrones, proporciona visibilidad de los riesgos de seguridad de los datos y permite establecer una protección automatizada contra esos riesgos.

Para ayudarlo a administrar la situación de seguridad del patrimonio de datos de Amazon Simple Storage Service (Amazon S3) de su organización, Macie le proporciona un inventario de sus cubos de S3 y los evalúa y monitorea automáticamente para garantizar la seguridad y el control de acceso. Si Macie detecta un posible problema con la seguridad o la privacidad de sus datos, como un bucket de acceso público, Macie genera un resultado para que lo revise y solucione según sea necesario.

Macie también automatiza el descubrimiento y la notificación de datos confidenciales para que pueda comprender mejor los datos que su organización almacena en Amazon S3. Para detectar datos confidenciales, puede utilizar los criterios y técnicas integrados que proporciona Macie, los criterios personalizados que usted defina o una combinación de ambos. Si Macie detecta datos confidenciales en un objeto de S3, Macie genera un hallazgo para notificarle los datos confidenciales que encontró Macie.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/22077c38-52f2-4e80-8d46-2d1ecb218deb">
</p>


## Características de Amazon Macie

Estas son algunas de las formas clave en las que Amazon Macie puede ayudarlo a descubrir, supervisar y proteger sus datos confidenciales en Amazon S3.

### Automatice el descubrimiento de datos confidenciales
Con Macie, puede automatizar el descubrimiento y la notificación de datos confidenciales de dos maneras: configurando Macie para que realice la detección automática de datos confidenciales y creando y ejecutando tareas de descubrimiento de datos confidenciales. Si Macie detecta datos confidenciales en un objeto de S3, crea automáticamente una búsqueda de datos confidenciales. El hallazgo proporciona un informe detallado de los datos confidenciales que encontró Macie.

### Descubra una variedad de tipos de datos confidenciales
Para descubrir datos confidenciales con Macie, puede utilizar criterios y técnicas integrados, como el aprendizaje automático y la coincidencia de patrones, para analizar los objetos de los cubos de S3. Estos criterios y técnicas, denominados identificadores de datos gestionados, pueden detectar una lista grande y creciente de tipos de datos confidenciales para muchos países y regiones, incluidos varios tipos de información de identificación personal (PII), datos financieros y datos de credenciales.

### Evalúe y supervise los datos para garantizar la seguridad y el control de acceso
Cuando habilitas Macie, Macie genera automáticamente y comienza a mantener un inventario completo de tus cubos de S3. Macie también comienza a evaluar y monitorear los cubos para garantizar la seguridad y el control de acceso. Si Macie detecta un posible problema con la seguridad o la privacidad de un bucket, crea una búsqueda de política para usted.

### Revisar y analizar los hallazgos
En Macie, un hallazgo es un informe detallado de los datos confidenciales que Macie detecta en un objeto de S3 o de un posible problema con la seguridad o la privacidad de un bucket de S3. Cada hallazgo proporciona una clasificación de la gravedad, información sobre el recurso afectado y detalles adicionales, como cuándo y cómo Macie detectó el problema.

### Supervise y procese los hallazgos con otros servicios y sistemas
Para facilitar la integración con otros servicios y sistemas, Macie publica sus hallazgos en Amazon EventBridge como eventos de búsqueda. EventBridgees un servicio de bus de eventos sin servidor que puede enrutar los datos de los hallazgos a destinos como AWS Lambda las funciones y los temas de Amazon Simple Notification Service (Amazon SNS). Con EventBridge él, puede supervisar y procesar los hallazgos casi en tiempo real como parte de sus flujos de trabajo actuales de seguridad y cumplimiento.

### Administre de forma centralizada varias cuentas de Macie
Si su AWS entorno tiene varias cuentas, puede administrar Macie de forma centralizada para las cuentas de su entorno. Puede hacerlo de dos maneras: integrando Macie con Macie AWS Organizations o enviando y aceptando invitaciones de membresía en Macie.

### Desarrollar y gestionar recursos mediante programación
Además de la consola de Amazon Macie, puede interactuar con Macie mediante la API de Amazon Macie. La API de Amazon Macie le brinda acceso completo y programático a la configuración, los datos y los recursos de su cuenta de Macie.

## References
- https://docs.aws.amazon.com/es_es/macie/latest/user/what-is-macie.html
