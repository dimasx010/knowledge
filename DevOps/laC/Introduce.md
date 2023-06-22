# Infraestructura como codigo laC

La infraestructura como código (IaC del inglés Infrastructure as Code) permite gestionar y preparar la infraestructura a través del código, en lugar de hacerlo mediante procesos manuales.

Con este tipo de infraestructura, se crean archivos de configuración que contienen las especificaciones que esta necesita, lo cual facilita la edición y la distribución de las configuraciones. Asimismo, garantiza que usted siempre prepare el mismo entorno. La infraestructura como código codifica y documenta sus especificaciones para facilitar la gestión de la configuración, y le ayuda a evitar los cambios ad hoc y no documentados.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/6b72487b-895b-4c12-9875-6138b51f584b">
</p>

El control de versiones es un aspecto importante de la infraestructura como código que debería aplicar a sus archivos de configuración, al igual que a cualquier otro archivo de código fuente del software. La implementación de la infraestructura como código también permite dividirla en elementos modulares que se combinarán de distintas maneras mediante la automatización.

Si se automatiza la preparación de la infraestructura con la infraestructura como código, los desarrolladores no tendrán que preparar ni gestionar manualmente los servidores, los sistemas operativos, el almacenamiento ni ningún otro elemento cada vez que desarrollen o implementen una aplicación. La codificación de su infraestructura le proporciona una plantilla que puede seguir durante la preparación. Si bien todavía se puede hacer de forma manual, una herramienta de automatización como Red Hat® Ansible® Automation Platform puede hacerlo por usted. 

## La diferencia entre los enfoques declarativo e imperativo de la Infrastructure as Code

Hay dos maneras de abordar la Infrastructure as Code: mediante un enfoque declarativo o uno imperativo. 

El enfoque declarativo define el estado deseado de los sistemas, lo cual incluye los recursos que usted necesita y las propiedades que deben tener dichos sistemas, y la herramienta de infraestructura como código se encargará de configurarlo por usted. 

Asimismo, detalla en una lista el estado actual de los objetos de su sistema, lo que facilita el desmontaje de la infraestructura.

En cambio, el enfoque imperativo define los comandos específicos para lograr la configuración deseada, los cuales se deben ejecutar en el orden correcto. 

Muchas herramientas de la infraestructura como código utilizan un enfoque declarativo y prepararán la infraestructura deseada de manera automática. Por lo tanto, si realiza modificaciones en el estado deseado, una herramienta de IaC declarativa las implementará por usted; pero si utiliza una herramienta imperativa, deberá resolver la manera de aplicar esos cambios.

La mayoría de las herramientas de la infraestructura como código pueden operar con ambos enfoques, pero tienden a dar prioridad a alguno de ellos.

## Ventajas de la Infrastructure as Code

La preparación de la infraestructura siempre había sido un proceso manual largo y costoso. En la actualidad, su gestión ha dejado de lado el hardware físico en los centros de datos, aunque todavía puede formar parte de los elementos de su empresa, pero en general se ha optado por la virtualización, los contenedores y el cloud computing. 

Con este último, aumentó la cantidad de elementos de la infraestructura y se comenzaron a lanzar más aplicaciones a la producción de forma regular. Además, requiere que la infraestructura se ponga en marcha, se amplíe y se desmonte con frecuencia. Si no se aplica una práctica dela infraestructura como código, resulta cada vez más difícil gestionar la ampliación de la infraestructura actual.

La infraestructura como código permite que su empresa gestione las necesidades de la infraestructura de TI al mismo tiempo que mejora la uniformidad y reduce los errores y la configuración manual.

### Ventajas:
- Reducción de costos
- Aumento en la velocidad de implementación
- Disminución de la cantidad de errores
- Mayor uniformidad de la infraestructura
- Eliminación de los desajustes de configuración

## Referencias
- https://www.redhat.com/es/topics/automation/what-is-infrastructure-as-code-iac