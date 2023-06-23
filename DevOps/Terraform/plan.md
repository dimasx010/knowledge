# Terraform Plan

Plan es otro de los comandos de Terraform de mayor importancia en la plataforma, debido a que tiene la capacidad de revisar toda la función y compararla con la infraestructura actual. El llamado comando Terraform Plan tiene la función de crear un plan de ejecución. Además, se encarga de llevar a cabo una actualización, a menos de que el usuario deshabilite esta opción de forma específica.

Básicamente terraform genera un plan de ejecución que describe lo que hará para alcanzar el estado deseado y luego lo ejecuta para construir la infraestructura descrita.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/9d51bb9c-354e-4c93-8030-d2566231bb4c">
</p>

Dentro de los parámetros opcionales de los comandos de Terraform se encuentran:

- lock=true: bloquea el archivo de estado cuando se admite el bloqueo.
- lock-timeout=0s : se refiere a la duración establecida para volver a intentar un bloqueo de estado.
- module-depth=n: se utiliza para especificar los módulos que se mostrarán en la salida. Esto no afecta al plan en sí, solo a la salida mostrada. De manera preestablecida, esto es -1, lo que ampliará todo.

## Referencias
- https://terraform-infraestructura.readthedocs.io/es/latest/comandos/
- https://galvarado.com.mx/post/tutorial-infraestructura-como-c%C3%B3digo-con-terraform/