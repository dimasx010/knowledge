# Terraform Modules

A medida que administre su infraestructura con Terraform, se crearán configuraciones cada vez más complejas. La complejidad de un archivo o directorio de configuración de Terraform no cuenta con un límite intrínseco, por lo que puede escribir y actualizar sus archivos de configuración en un único directorio. Sin embargo, si lo hace, es posible que experimente uno o varios de los siguientes problemas:

Comprender los archivos de configuración y navegar por ellos será cada vez más difícil.

Actualizar la configuración será cada vez más riesgoso, ya que la actualización de un bloque podría traer consecuencias inesperadas a otros bloques de su configuración.

La duplicación de bloques de configuración similares podría aumentar, por ejemplo, cuando configure entornos independientes de desarrollo, etapa de pruebas o producción. Esto aumentará la carga cuando actualice esas partes de su configuración.

Si desea compartir partes de su configuración con otros proyectos y equipos, cortar y pegar los bloques de configuración en distintos proyectos podría provocar errores y sería una operación difícil de mantener.

En este lab, descubrirá cómo los módulos pueden encargarse de estos problemas, así como la estructura de un módulo de Terraform y las prácticas recomendadas para crearlos y usarlos.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/34cde74b-edb7-4bcc-849d-1d80a6dd6685">
</p>

## ¿Para qué sirven los módulos?

Estas son algunas de las maneras en que los módulos le permiten solucionar los problemas enumerados anteriormente:

### Organice la configuración

Los módulos facilitan la navegación, comprensión y actualización de su configuración, ya que agrupan sus partes relacionadas. Incluso una infraestructura con una complejidad moderada puede requerir cientos o miles de líneas de configuración para implementarse. Sin embargo, si usa módulos, puede organizar su configuración en componentes lógicos.

### Encapsule la configuración

Otro beneficio de usar módulos es que puede encapsular la configuración en componentes lógicos separados. La encapsulación permite evitar consecuencias inesperadas (por ejemplo, que un cambio en una parte de su configuración modifique otra infraestructura por accidente) y reduce las probabilidades de que se produzcan errores sencillos, como usar el mismo nombre para dos recursos diferentes.

### Reutilice la configuración

Escribir su configuración completa sin usar el código existente puede tardar mucho y provocar errores. En cambio, si usa módulos puede ahorrar tiempo y reducir los errores costosos, ya que se reutiliza la configuración escrita por usted, otros miembros de su equipo, o bien otros profesionales de Terraform que publicaron módulos para que los utilice. También puede compartir los módulos que escriba con su equipo o el público general para que se beneficien de su arduo trabajo.

### Proporcione coherencia y asegúrese de que se apliquen las prácticas recomendadas

Los módulos también lo ayudan a proporcionar coherencia a sus configuraciones. La coherencia permite que los parámetros de configuración complejos sean más fáciles de comprender, y esto garantiza que se apliquen las prácticas recomendadas en toda su configuración. Por ejemplo, los proveedores de servicios en la nube ofrecen varias opciones para configurar servicios de almacenamiento de objetos, como Amazon S3 (Simple Storage Service) o los buckets de Google Cloud Storage. Muchos incidentes de seguridad de alto perfil han implicado el almacenamiento de objetos con errores de protección. Debido a la cantidad de opciones complejas de configuración involucradas, es fácil configurar incorrectamente estos servicios de manera accidental.

## Referencias
- https://www.plainconcepts.com/es/terraform/