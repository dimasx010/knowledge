# AWS Organizations

AWS Organizations es un servicio de gestión de cuentas que le permite consolidar varias Cuentas de AWS en una organización que cree y administre de forma centralizada. AWS Organizations incluye todas las prestaciones de facturación unificada y posibilidades de administración de cuentas para que pueda satisfacer mejor las necesidades presupuestarias, de seguridad y de conformidad de su negocio. Como administrador de su organización, puede crear cuentas e invitar a cuentas existentes a unirse a la organización.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/5b9e86e0-e513-451a-8cd4-15a65a36eb29">
</p>

## Características de AWS Organizations

### AWS Organizations ofrece las siguientes características:

Administración centralizada de todas sus Cuentas de AWS
Puede combinar sus cuentas existentes en una organización para poder administrar las cuentas de forma centralizada. Puede crear cuentas que se conviertan automáticamente en parte de su organización y puede invitar a otras cuentas a que se unan a su organización. También puede asociar políticas que afecten a algunas o a todas sus cuentas.

### Facturación unificada para todas las cuentas miembro

La facturación unificada es una característica de AWS Organizations. Puede utilizar la cuenta de administración de su organización para consolidar y pagar los gastos de todas las cuentas miembro. En la facturación unificada, las cuentas de administración también pueden acceder a la información de facturación, la información de la cuenta y la actividad de las cuentas miembro de su organización. Esta información se puede utilizar para servicios como Cost Explorer, lo que puede ayudar a las cuentas de administración a mejorar el rendimiento de los costos de su organización.

### Agrupar jerárquicamente todas sus cuentas para satisfacer sus necesidades presupuestarias, de seguridad y de conformidad

Puede agrupar sus cuentas en unidades organizativas y asociar diferentes políticas de acceso a cada una de ellas. Por ejemplo, si tiene cuentas que deben tener acceso solo a los servicios de AWS que cumplan determinados requisitos normativos, puede incluirlas en una unidad organizativa. A continuación, puede asociar una política a esa unidad organizativa que bloquee el acceso a los servicios que no cumplan los requisitos normativos. Puede anidar unidades organizativas en otras unidades organizativas, hasta un máximo de cinco niveles de profundidad, lo que proporciona flexibilidad en el modo de estructurar sus grupos de cuentas.

### Políticas para centralizar el control de los servicios de y las acciones de la API de AWS a las que puede tener acceso cada cuenta

Como administrador de la cuenta de administración de una organización, puede utilizar políticas de control de servicios (SCP) para especificar el número máximo de permisos de las cuentas de los miembros de la organización. En las SCP, puede restringir a qué servicios, recursos y acciones de API individuales de AWS pueden obtener acceso los usuarios y roles de cada cuenta de miembro. También puede definir condiciones respecto a cuándo restringir el acceso a los servicios, los recursos y las acciones de la API de AWS. Estas restricciones se aplican incluso a los administradores de las cuentas miembro de la organización. Cuando AWS Organizations bloquea el acceso a una acción de la API, un recurso o un servicio en una cuenta de miembro, un usuario o rol de dicha cuenta no puede acceder a ella. Este bloqueo permanece en vigor aunque un administrador de una cuenta de miembro conceda dichos permisos de forma explícita en una política deI IAM.

### Políticas para estandarizar etiquetas en los recursos de las cuentas de su organización.

Puede utilizar políticas de etiquetas para mantener la coherencia de las etiquetas, incluido el tratamiento de casos preferentes de valores y claves de etiquetas.

### Políticas para controlar cómo la inteligencia artificial (IA) AWS y los servicios de Machine Learning pueden recopilar y almacenar datos.

Puede utilizar las políticas de exclusión de los servicios de IA para optar por no participar en la recopilación y el almacenamiento de datos para cualquiera de los servicios de IA AWS que no quiera utilizar.

### Políticas que configuran copias de seguridad automáticas de los recursos de las cuentas de su organización

Puede usar políticas de copia de seguridad para configurar y aplicar automáticamente los planes AWS Backup de recursos de todas las cuentas de su organización.

### Integración y compatibilidad con AWS Identity and Access Management (IAM)

IAM permite un control pormenorizado de los usuarios y las funciones en las cuentas individuales. AWS Organizations amplía ese control al nivel de cuenta para permitirle controlar lo que los usuarios y las funciones de una cuenta o grupo de cuentas pueden hacer. Los permisos resultantes son la intersección lógica de lo que permite AWS Organizations en el nivel de cuenta y los permisos que IAM concede explícitamente en el nivel de usuario o de rol dentro de esa cuenta. En otras palabras, el usuario solo puede tener acceso a lo que permiten tanto las políticas de AWS Organizations como las políticas deI IAM. Si alguna bloquea una operación, el usuario no puede tener acceso a esa operación.

### Integración con otros servicios de AWS

Puede aprovechar los servicios de administración de varias cuentas de AWS Organizations con servicios seleccionados de AWS para realizar tareas en todas las cuentas que son miembros de su organización. Para obtener una lista de los servicios y los beneficios de utilizar cada servicio en la organización

### Acceso global

AWS Organizations es un servicio global con un único punto de enlace que funciona desde cualquier Regiones de AWS. No es necesario seleccionar de forma explícita una región en la que operar.

### Uso gratuito

AWS Organizations es una característica de su Cuenta de AWS que se ofrece sin cargo adicional. Solo se le cobrará cuando acceda a otros servicios AWS de las cuentas de su organización

## References
- https://docs.aws.amazon.com/es_es/organizations/latest/userguide/orgs_introduction.html
