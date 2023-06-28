# AWS Identity and Access Management (IAM)

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/ac593bfc-69cb-4fb6-a7d1-efe3d3e0ab63">
</p>

AWS Identity and Access Management (IAM) is a web service that helps you securely control access to AWS resources. With IAM, you can centrally manage permissions that control which AWS resources users can access. Use IAM; to control who is authenticated (logged in) and authorized (has permissions) to use resources.

When you create an AWS Account, you start with a login identity that has full access to all AWS resources and Services in the account. This identity is given the AWS Account root user name and is accessed by logging in with the email and password you used to create the account. We recommend that you do not use the root user for everyday tasks. Protect the root user credentials and use them only for tasks that the root user can perform. For a complete list of tasks that require you to log in as the root user, see Tasks that require root user credentials in the AWS Account Management Reference Guide.

Se recomienda básicamente generar las configuraciones sobre los usuarios por medio de los grupos, configuramos los mismos, y asociamos los usuarios a los mencionados grupos, esto facilita la gestión cuando se le da de baja a un usuario o este es movido de un puesto a otro. 

Adicional a ello, se recomienda configurar la autenticación multifactor para la cuenta root, e incluso al iniciar se recomienda no utilizar la cuenta root sino configurar un usuario tipo administrador para realizar las gestiones pertinentes, esto es fundamental ya que el mismo puede ser parametrizable, a excepción del usuario root. 

## Características de IAM

Para ayudar a controlar el acceso y administrar las identidades de su cuenta de AWS, IAM ofrece muchas características para garantizar la seguridad.

- IAM es global y no es específica de ninguna región. Puede ver y utilizar las configuraciones de IAM desde cualquier región en la consola de administración de AWS.
- IAM se integra en muchos servicios de AWS de forma predeterminada.
Puede establecer políticas de contraseñas en IAM a fin de especificar los requisitos de complejidad y los periodos de rotación obligatorios para los usuarios.
- IAM admite MFA.
- IAM admite la identidad federada, que permite a los usuarios que ya tienen contraseñas en otro lugar (p. ej.: en su red corporativa o con un proveedor de identidad de Internet) obtener acceso temporal a su cuenta de AWS.
Cualquier cliente de AWS puede utilizar IAM; el servicio se ofrece sin cargo adicional.

## Usuario de IAM

Un usuario de IAM representa a la persona o el servicio que interactúa con AWS. Puede definir el usuario de su cuenta de AWS. Se factura a su cuenta cualquier actividad realizada por ese usuario. Una vez creado un usuario, ese usuario puede iniciar sesión para acceder a los recursos de AWS de su cuenta.

También puede añadir más usuarios a la cuenta según sea necesario. Por ejemplo, para la aplicación de fotos de gatos, podría crear usuarios individuales en su cuenta de AWS que correspondan a las personas que están trabajando en su aplicación. Cada persona debe tener sus propias credenciales de inicio de sesión. Proporcionar a los usuarios sus propias credenciales de inicio de sesión impide compartir las credenciales.

## Roles de IAM

Mantener roles es más eficiente que mantener a los usuarios. Cuando asume un rol, IAM proporciona dinámicamente credenciales temporales que vencen tras un periodo definido, entre 15 minutos y 36 horas. Los usuarios, por otro lado, tienen credenciales de largo plazo en forma de combinaciones de nombre de usuario y contraseña, o un conjunto de claves de acceso.

Las claves de acceso de usuario solo vencen cuando usted o el administrador de la cuenta rotan las claves. Las credenciales de inicio de sesión de usuario caducan si aplica una política de contraseñas a su cuenta que obliga a los usuarios a rotar las contraseñas.

## Proveedores de identidad (IdP)

Si decide convertir su aplicación de fotos de gatos en un negocio y comienza a tener más de unas personas trabajando en ella, considere administrar la información de identidad de los empleados a través de un proveedor de identidad (IdP). El uso de un IdP, ya sea un servicio de AWS, como AWS Single Sign-On o un proveedor de identidad de terceros, proporciona una fuente única de información para todas las identidades de su organización.

Ya no tiene que crear usuarios de IAM independientes en AWS. En cambio, puede utilizar roles de IAM para proporcionar permisos a las identidades federadas de su IdP. Por ejemplo, hay una empleada, Martha, que tiene acceso a varias cuentas de AWS. En lugar de crear y administrar varios usuarios de IAM llamados “Martha” en cada una de esas cuentas de AWS, podría administrar Martha en el IdP de su empresa. Si Martha cambia a otro puesto en la empresa o la abandona, se puede actualizar en el IdP, en lugar de en todas las cuentas de AWS de la empresa.

Si tiene una organización que abarca muchos empleados y varias cuentas de AWS, es posible que desee que sus empleados inicien sesión con una única credencial.

AWS SSO es un IdP que permite a los usuarios iniciar sesión en un portal de usuarios con un único conjunto de credenciales. A continuación, proporciona a los usuarios acceso a sus cuentas y aplicaciones asignadas en una ubicación central.

Es similar a IAM. AWS SSO ofrece un directorio en el que puede crear usuarios, organizarlos en grupos, establecer permisos en todos los grupos y conceder acceso a los recursos de AWS. Sin embargo, AWS SSO tiene algunas ventajas en comparación con IAM. Por ejemplo, si utiliza un IdP de terceros, puede sincronizar sus usuarios y grupos con AWS SSO. Esto elimina la carga de volver a crear usuarios que ya existen en otro lugar y le permite administrar los usuarios desde su IdP. Lo más importante es que AWS SSO separa las tareas entre su IdP y AWS, lo que garantiza que la administración del acceso a la nube no esté en el IdP ni dependa de él.

## Credenciales de usuario de IAM

Un usuario de IAM consta de un nombre y un conjunto de credenciales. Al crear un usuario, puede proporcionarle los siguientes tipos de acceso:

- Acceso a la consola de administración de AWS
- Acceso programático a AWS Command Line Interface (AWS CLI) y a la interfaz de programación de la aplicación de AWS (API de AWS)

Para acceder a la consola de administración de AWS, proporcione al usuario un nombre de usuario y una contraseña. Para el acceso mediante programación, AWS genera un conjunto de claves de acceso que se puede utilizar con AWS CLI y la API de AWS. Las credenciales de usuario de IAM se consideran permanentes, lo que significa que se mantienen con el usuario hasta que los administradores hagan una rotación forzada.

Cuando crea un usuario de IAM, puede conceder permisos directamente a nivel de usuario. Esto puede parecer una buena idea si solo tiene un usuario o unos usuarios. Sin embargo, a medida que aumenta el número de usuarios, mantenerse al día con los permisos puede ser más complicado. Por ejemplo, si tiene 3000 usuarios en su cuenta de AWS, puede ser un desafío administrar el acceso y obtener una visión general de quién puede realizar qué acciones en cuáles recursos.

Si tan solo existiera una forma de agrupar los usuarios de IAM y en cambio adjuntar los permisos a nivel de grupo. Adivine qué. Existe.

## Grupos de IAM

Un grupo de IAM es una colección de usuarios. Todos los usuarios del grupo heredan los permisos asignados al grupo. Esto permite conceder permisos a varios usuarios a la vez. Es una forma más conveniente y escalable de administrar los permisos de los usuarios de su cuenta de AWS. Por eso, es una práctica recomendada utilizar grupos de IAM.

Si está tratando de crear una aplicación y hay varios usuarios en una cuenta que trabajan en la aplicación, puede organizarlos por función de trabajo. Por ejemplo, puede organizar los grupos de IAM por desarrolladores, seguridad y administradores. A continuación, puede colocar a todos los usuarios de IAM en sus respectivos grupos.

Esto proporciona una forma de ver quién tiene qué permisos en su organización. También lo ayuda a escalar cuando las nuevas personas se unen o se van, y cuando cambian de roles en su organización.

Tenga en cuenta los siguientes ejemplos:

- Un nuevo desarrollador se une a su cuenta de AWS para ayudarlo con su aplicación. Crea un nuevo usuario y lo añade al grupo de desarrolladores, sin pensar qué permisos necesitan.
- Un desarrollador cambia de trabajo y se convierte en ingeniero de seguridad. En lugar de editar los permisos del usuario directamente, lo elimina del grupo anterior y lo añade al nuevo grupo que ya tiene el nivel de acceso correcto.

Tenga en cuenta las siguientes características de los grupos:

- Los grupos pueden tener muchos usuarios.
- Los usuarios pueden pertenecer a muchos grupos.
- Los grupos no pueden pertenecer a grupos.

El usuario raíz puede realizar todas las acciones en todos los recursos de una cuenta de AWS de forma predeterminada. Esto contrasta con la creación de nuevos usuarios de IAM, nuevos grupos o roles. Las nuevas identidades de IAM no pueden realizar acciones en su cuenta de AWS de forma predeterminada hasta que les conceda permiso explícitamente.

La forma en que concede permisos en IAM es mediante las políticas de IAM.

## Políticas de IAM

Para administrar el acceso y proporcionar permisos a los servicios y recursos de AWS, crea políticas de IAM y las adjunta a los usuarios, grupos y roles de IAM. Cada vez que un usuario o rol hace una solicitud, AWS evalúa las políticas asociadas a ellos. Por ejemplo, si hay un desarrollador en el grupo de desarrolladores que solicita un servicio de AWS, AWS evalúa las políticas adjuntas al grupo de desarrolladores y las políticas adjuntas al usuario de desarrollador para definir si la solicitud debe permitirse o denegarse.

## References
- https://docs.aws.amazon.com/en_en/IAM/latest/UserGuide/introduction.html
