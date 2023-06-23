# Terraform information

Terraform es una herramienta de configuración de software diseñada para potenciar la automatización de múltiples procesos a través de conceptos como el de infrastructure as code. A través de su lenguaje permite crear definiciones (llamadas resources) de objetos o recursos de infraestructura.

Su principal objetivo es facilitar la creación de infraestructura de manera declarativa, por ejemplo un centro de datos en servicios como Azure, Amazon Web Services (AWS) o Google Cloud Platform (GCP). Es decir, esta configuración se almacena en la nube y permite automatizar una infraestructura.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/e98e7671-9939-4d3c-8bdb-d182d39a3087">
</p>

## Terraform consta de elementos como:

Núcleo Terraform. Consiste en recibir la información y tomar decisiones con ella.
Proveedores. Son las herramientas con las que se crea la infraestructura.

## ¿Qué se puede hacer con Terraform?

La propia web de Terraform propone varios escenarios en los que se podría usar esta tecnología:

Automatización de la infraestructura digital: servidores, bases de datos, firewall…

Administrar un entorno multinube (AWS, Azure, GCP…) a pesar de sus diferentes interfaces o flujos de trabajo. Esto es ideal cuando el entorno se ha construido antes de implantar Terraform y hay que administrar diferentes entornos cloud. En cualquier caso, también puede administrar una sola aplicación y de un solo proveedor.

Gestionar clústeres de Kubernetes e imágenes de máquinas virtuales. Sobre estas últimas, HCP 

Packer recopila imágenes de entornos multinube y las puede suministrar para una API.

Las configuraciones se pueden compartir y volver a usar cuando se crea necesario.

Desde la web de Terraform es posible acceder a su código abierto y contribuir a este proyecto colaborativo.

## Beneficios de Terraform para empresas

Uno de los principales beneficios de Terraform para empresas es que, al tener un lenguaje declarativo que abstrae los recursos de múltiples proveedores cloud (como los muy populares Azure, AWS y GCP) bajo una sintaxis común, facilita la implementación de infraestructura de manera mucho más ágil, con menos coste en tiempo y adaptación por parte del desarrollador. Además, esto permite que la infraestructura se pueda trasladar a otro servicio.

Asimismo, como veíamos antes, Terraform ayuda en la cada vez más atractiva automatización de las empresas. La automatización del flujo de trabajo se puede llevar a muy diferentes departamentos e integrarse a sus dinámicas. Este mismo flujo permite un fuerte control de la seguridad, con controles de acceso a la información.

Por otra parte, el lenguaje que usa, llamado HCL (lenguaje de configuración de HashiCorp, por la empresa creadora), es muy sencillo de usar, lo que facilita su uso. Y por si estos fueran pocos beneficios, recordemos que Terraform funciona con un código que es abierto y que, además, se puede descargar para ejecutar localmente

## Referencias
- https://www.plainconcepts.com/es/terraform/