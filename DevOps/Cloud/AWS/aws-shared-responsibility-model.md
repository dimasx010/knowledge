# AWS Shared Responsibility Model

Básicamente este nos expone teórica la responsabilidad en cuanto a la infra que implementemos en esa plataforma, en la siguiente imagen podremos analizar el mencionado modelo. 

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/d6198954-788a-4631-b63a-c4e501bd0a43">
</p>

## Responsabilidad de AWS

AWS es responsable de la seguridad de la nube. Esto significa que AWS proporciona seguridad y protección a la infraestructura que ejecuta los servicios ofrecidos en la nube de AWS. AWS es responsable de lo siguiente:

- Proporcionar seguridad y protección a las regiones, las zonas de disponibilidad y los centros de datos de AWS, hasta la seguridad física de los edificios

- Administrar el hardware, el software y los componentes de redes que ejecutan los servicios de AWS, como los servidores físicos, los sistemas operativos del host, las capas de virtualización y los componentes de redes de AWS

El nivel de responsabilidad de AWS depende del servicio. AWS clasifica los servicios en tres categorías. En la siguiente tabla, se proporciona información sobre cada uno, incluida la responsabilidad de AWS

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/6abdee78-04b4-461a-a77b-a9204f7e694e">
</p>

Nota: Los servicios de contenedores hacen referencia a los contenedores de aplicaciones abstractos de AWS en segundo plano, no a los servicios de contenedores de Docker. Esto permite a AWS quitar a los clientes la responsabilidad de administrar la plataforma.

## Responsabilidad del cliente

Los clientes son responsables de la seguridad en la nube. Al utilizar cualquier servicio de AWS, es responsable de configurar correctamente el servicio y las aplicaciones, además de garantizar que sus datos estén seguros.

Su nivel de responsabilidad depende del servicio de AWS. Algunos servicios requieren que realice todas las tareas de administración y configuración de seguridad necesarias, mientras que otros servicios más abstractos requieren que solo administre los datos y controle el acceso a los recursos. Con las tres categorías de servicios de AWS, puede definir su nivel de responsabilidad por cada servicio de AWS que utilice.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/dbbb13ce-321b-46aa-8f10-9ac730f73367">
</p>

Debido a los distintos niveles de esfuerzo, los clientes deben considerar qué servicios de AWS utilizan y revisar el nivel de responsabilidad necesario para proteger cada servicio. También deben revisar cómo el modelo de seguridad compartida se ajusta a los estándares de seguridad de su entorno de TI, además de las leyes y reglamentos aplicables.

Un concepto clave es que los clientes mantienen el control total de los datos y son responsables de administrar la seguridad relacionada con su contenido. Por ejemplo, usted es responsable de lo siguiente:

- Elegir una región para los recursos de AWS de acuerdo con las normas de soberanía de datos
- Implementar mecanismos de protección de datos, como el cifrado y las copias de seguridad programadas
- Utilizar el control de acceso para limitar quién puede acceder a los datos y recursos de AWS

## References
- https://keepcoding.io/blog/regiones-y-zonas-de-disponibilidad-de-aws/
- https://aws.amazon.com/en/about-aws/global-infrastructure/?p=ngi&loc=1