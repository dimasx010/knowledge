# Gestión de Secretos

Las empresas digitales de hoy en día dependen de aplicaciones comerciales, desarrolladas internamente y de código abierto para llevar a cabo sus negocios y se sirven cada vez más de la infraestructura de TI automatizada y de las metodologías de DevOps para acelerar el desarrollo y la innovación. Aunque los entornos de aplicaciones y de TI varían considerablemente de una organización a otra, una cosa se mantiene constante: cada aplicación, script, herramienta de automatización y otra identidad no humana depende de alguna forma de credencial con privilegios para acceder a otras herramientas, aplicaciones y datos.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/c916cffb-9812-4cc9-8366-4cc8eab3a0ca">
</p>

## ¿Qué es un secreto?

Estas credenciales no humanas con privilegios suelen denominarse «secretos» y hacen referencia a una información privada que actúa como llave para desbloquear recursos protegidos o información sensible en herramientas, aplicaciones, contenedores, entornos de DevOps y entornos nativos en la nube.

Entre los tipos más comunes de secretos se incluyen:

Credenciales de cuentas con privilegios
- Contraseñas
- Certificados
- Claves SSH
- Claves de API
- Claves de cifrado

## Principales desafíos a la hora de gestionar secretos

Un usuario no humano con acceso a un secreto obtiene automáticamente acceso y permisos en tiempo real a cualquier recurso que pertenezca al propietario del secreto. Los ciberdelincuentes son conscientes de esto y dirigen sus ataques a secretos para obtener acceso no autorizado a otros secretos y hosts a fin de completar su misión. Un ciberataque dirigido a secretos a menudo se extiende mucho más allá del alcance de la brecha inicial.

Los secretos son generalizados. Entre ellos figuran credenciales incrustadas en el código fuente de aplicaciones de contenedor (por ejemplo, Red Hat OpenShift, Kubernetes o Pivotal); procesos de automatización (por ejemplo, Ansible Playbooks, Puppet o Chef); aplicaciones vitales para la empresa, tanto las desarrolladas a nivel interno como las disponibles en el mercado (COTS); software de seguridad, como escáneres de vulnerabilidad; servidores de aplicaciones y software de gestión de TI; plataformas de automatización robótica de procesos (RPA) y la cadena de herramientas de integración continua/implementación continua (CI/CD).

Los procesos automatizados son increíblemente potentes. Pueden acceder a datos protegidos, ampliarse a una velocidad sin precedentes, aprovechar los recursos en la nube y ejecutar procesos empresariales de forma instantánea. Pero, tal como demuestran las filtraciones de ciberseguridad que han acaparado titulares, los procesos automatizados son susceptibles de sufrir ciberataques sofisticados, que pueden ocurrir de repente y propagarse rápidamente. Las organizaciones deben proteger los secretos asignados a las identidades no humanas para defenderse de los ataques y mitigar los riesgos.

## ¿Qué es la gestión de secretos?

La gestión de secretos, una de las prácticas recomendadas de ciberseguridad para las empresas digitales, permite a las organizaciones aplicar sistemáticamente políticas de seguridad para las identidades no humanas. La gestión de secretos garantiza que solo las entidades autenticadas y autorizadas puedan acceder a los recursos de las pilas de herramientas, plataformas y entornos en la nube.

Los siguientes pasos se suelen incluir en una iniciativa de gestión de secretos. Muchos de estos enfoques y técnicas se utilizan también para proteger el acceso con privilegios por parte de usuarios humanos.

- Autenticar todas las solicitudes de acceso que utilicen credenciales no humanas.
- Implementar el principio del mínimo privilegio.
- Aplicar el control de acceso basado en roles (RBAC) y rotar regularmente los secretos y credenciales.
- Automatizar la gestión de los secretos y aplicar políticas de acceso coherentes.
- Realizar un seguimiento de todos los accesos y mantener una auditoría completa.
- Eliminar los secretos del código, los archivos de configuración y otras áreas desprotegidas.

## Casos de uso comunes en la gestión de secretos

### Gestión de secretos para proteger los procesos de CI/CD. 
Las herramientas populares de procesos de CI/CD como Jenkins, Ansible, Puppet y Chef están diseñadas para lograr eficiencia y velocidad, pero pueden presentar nuevos retos de seguridad. Estas herramientas automatizadas de gestión de la configuración requieren secretos para acceder a recursos protegidos como bases de datos, servidores SSH y servicios HTTP. Estos secretos suelen estar incrustados en el código fuente de forma no segura o estar almacenados en archivos de configuración o código para estas herramientas (por ej., JenkinsFiles, playbooks, scripts o código fuente). Una gestión de secretos eficaz permite a las organizaciones eliminar estos secretos codificados de las herramientas de DevOps de los procesos de CI/CD, a la vez que ofrece registros de auditoría completos, RBAC basado en políticas y rotación de secretos.

### Gestión de secretos para proteger contenedores. 
Los equipos de DevOps e ingeniería dependen cada vez más de los contenedores para acelerar el desarrollo y mejorar la portabilidad y la productividad. Los contenedores requieren secretos para acceder a información crítica y sensible. Sin embargo, como los contenedores son efímeros (o de corta duración), pueden ser difíciles de monitorizar y el acceso a recursos específicos puede resultar difícil de gestionar y proteger. Las medidas de seguridad de la gestión de secretos permiten a los equipos autenticar solicitudes de contenedor para secretos con atributos de plataformas nativas de contenedor y gestionar secretos con políticas RBAC para obtener un control granular.

### Gestión de secretos para administrar entornos elásticos y de escalado automático.
Los proveedores de la nube ofrecen funciones de escalado automático que permiten la elasticidad (efímera) y el modelo de pago a medida que crece la empresa. Si bien esto mejora la eficiencia, también crea nuevos desafíos de gestión de la seguridad, en particular en lo que respecta a la escalabilidad. Implementando prácticas recomendadas de gestión de secretos, las organizaciones pueden eliminar la necesidad de que los operadores humanos apliquen manualmente políticas a cada host nuevo al asignar una identidad al host en tiempo real y autenticar de forma segura la aplicación de llamada en función de la política de seguridad predefinida.

### Gestión de secretos para proteger las aplicaciones desarrolladas internamente y las aplicaciones COTS.
Las aplicaciones y scripts desarrollados internamente, junto con herramientas y soluciones de terceros como herramientas de seguridad, RPA, herramientas de automatización y de gestión de TI, a menudo requieren altos niveles de acceso con privilegios en toda la infraestructura de la empresa para completar sus tareas definidas. Las prácticas eficaces de gestión de secretos requieren que se eliminen las credenciales incrustadas en el código fuente de las aplicaciones y scripts desarrollados a nivel interno y que todos los secretos se almacenan, gestionan y roten de forma centralizada para reducir al mínimo los riesgos.

## Referencias
- https://www.cyberark.com/es/what-is/secrets-management/#:~:text=%C2%BFQu%C3%A9%20es%20un%20secreto%3F,entornos%20nativos%20en%20la%20nube.