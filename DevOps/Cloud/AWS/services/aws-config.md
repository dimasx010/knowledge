# AWS Amplify

AWS Config proporciona una vista detallada de la configuración de los recursos de AWS de su cuenta de AWS. Esto incluye cómo se relacionan los recursos entre sí y cómo se han configurado en el pasado, para que pueda ver cómo las configuraciones y las relaciones cambian a lo largo del tiempo.

unAWS recurso de es una entidad con la que se puede trabajar enAWS, como una instancia de Amazon Elastic Compute Cloud (EC2), un volumen de Amazon Elastic Block Store (EBS), un grupo de seguridad o una Amazon Virtual Private Cloud (VPC). Para obtener una lista completa de los recursos de AWS admitidos por AWS Config


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/e1767900-809d-4330-a303-287021ed79c2">
</p>

Al configurar AWS Config, puede completar lo siguiente:

## Gestión de recursos

- Especificar los tipos de recursos que desea que registre AWS Config.

- Configure un bucket de Amazon S3 para recibir una instantánea de configuración a solicitud y el historial de configuración.

-Configure Amazon SNS para enviar notificaciones de flujo de configuración.

- AWS ConfigConcédale los permisos que necesita para acceder al bucket de Amazon S3 y el tema de Amazon SNS.

## Paquetes de reglas y conformidad

- Especifique las reglas que desea que utilice AWS Config para evaluar la información de conformidad para los tipos de recursos registrados.

- Utilice paquetes de conformidad o un conjunto deAWS Config reglas y acciones de corrección que se puedan implementar y monitorear como una sola entidad en suAWS cuenta.

## Agregadores

- Utilice un agregador para obtener una vista centralizada de su inventario de recursos y cumplimiento. Un agregador es un tipo deAWS Config recurso que recopila datos deAWS Config configuración y cumplimiento de variasAWS cuentas yAWS regiones en una sola cuenta y región.

## Consultas avanzadas

Utilice una de las consultas de ejemplo o escriba su propia consulta consultando el esquema de configuración delAWS recurso.

## Modos de utilizar AWS Config

Cuando ejecuta sus aplicaciones en AWS, normalmente utiliza recursos de AWS que debe crear y administrar colectivamente. A medida que sigue aumentando la demanda de su aplicación, también lo hace la necesidad de realizar un seguimiento de sus recursos de AWS. AWS Config se ha diseñado para ayudarle a supervisar sus recursos de la aplicación en los siguientes casos:

## Administración de recursos

Para ejercer un mejor control de las configuraciones de sus recursos y detectar configuraciones erróneas de los mismos, necesita una visibilidad minuciosa sobre los recursos que existen y cómo dichos recursos están configurados en cualquier momento. Puede utilizar AWS Config para que se le notifique cuando se crean, modifican o eliminan recursos sin tener que supervisar estos cambios sondeando las llamadas realizadas a cada recurso.

Puede utilizar reglas de AWS Config para evaluar los ajustes de configuración de sus recursos de AWS. Cuando AWS Config detecta que un recurso infringe las condiciones en una de las reglas,AWS Config marca el recurso como no conforme y envía una notificación. AWS Config evalúa continuamente los recursos a medida que se crean, modifican o eliminan.

## Auditoría y conformidad

Es posible que trabaje con datos que requieren auditorías frecuentes para garantizar la conformidad con las políticas internas y las prácticas recomendadas. Para demostrar la conformidad, necesita acceder a las configuraciones históricas de los recursos. Esta información la proporciona AWS Config.

Administración y resolución de problemas de cambios de configuración
Al utilizar varios recursos de AWS que dependen unos de otros, un cambio en la configuración de un recurso podría tener consecuencias imprevistas en los recursos relacionados. Con AWS Config, puede ver cómo el recurso que va a modificar está relacionado con otros recursos y evaluar el impacto del cambio.

También puede utilizar las configuraciones históricas de los recursos proporcionadas por AWS Config para solucionar problemas y para acceder a la última configuración correcta conocida de un recurso con problemas.

## Análisis de seguridad

Para analizar las posibles debilidades de seguridad, necesita información histórica detallada sobre las configuraciones de sus AWS recursos, como los permisos AWS Identity and Access Management (de IAM) que se otorgan a sus usuarios o las reglas del grupo de seguridad de Amazon EC2 que controlan el acceso a sus recursos.

Puede utilizar AWS Config para ver la política de IAM que se asignó a un usuario, grupo o rol en cualquier momento durante el que AWSco Config se estaba grabando. Esta información puede ayudarle a determinar los permisos que pertenecían a un usuario en un momento específico: por ejemplo, puede ver si el usuario John Doe tenía permiso para modificar la configuración de Amazon VPC el 1 de enero de 2015.

También puede utilizar AWS Config para ver la configuración de los grupos de seguridad de EC2, incluidas las reglas de puertos que estaban abiertas en un momento concreto. Esta información puede ayudarle a determinar si un grupo de seguridad ha bloqueado el tráfico entrante de TCP a un puerto específico

## References
- https://docs.aws.amazon.com/es_es/config/latest/developerguide/WhatIsConfig.html
