# Amazon CloudShell (AWS)

AWS CloudShell es un shell previamente autenticado y basado en el navegador, que se puede lanzar directamente desde la página web de la AWS Management Console. Puede navegar CloudShell desde AWS Management Console varias formas diferentes. 

Al iniciar AWS CloudShell, se crea un entorno informático basado en Amazon Linux 2. En este entorno, puede acceder a una amplia gama de herramientas de desarrollo preinstaladas, opciones para cargar y descargar archivos y un almacenamiento de archivos que persiste entre sesiones.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b897123c-eda7-4b3c-8a07-32301e18dc4e">
</p>

## Características de AWS CloudShell

### AWS Command Line Interface

Puede iniciar AWS CloudShell desde AWS Management Console. Las AWS credenciales que utilizó para iniciar sesión en la consola están disponibles automáticamente en una nueva sesión de shell. Como AWS CloudShell los usuarios se autentican previamente, no es necesario configurar las credenciales al interactuar Servicios de AWS con AWS CLI la versión 2. AWS CLI Está preinstalado en el entorno de cómputos del shell.

### Conchas y herramientas de desarrollo

Con la consola que se crea para AWS CloudShell las sesiones, puede cambiar sin problemas entre sus shell de línea de comandos preferidas. Más específicamente, puede cambiar entre BashPowerShell, y Z shell. También tiene acceso a herramientas y utilidades preinstaladas.

El entorno de shell está preconfigurado y es compatible con varios de los principales lenguajes de software, como Node.js y Python. Esto significa que, por ejemplo, puede ejecutar Node.js oPython proyectos sin realizar primero instalaciones en tiempo de ejecución. PowerShelllos usuarios pueden usar el.NET Core tiempo de ejecución.

Puede confirmar los archivos que se creen o se AWS CloudShell carguen en un repositorio local antes de enviarlos a un repositorio remoto gestionado por AWS CodeCommit.

Para obtener más información, consulte AWS CloudShell entorno de cómputos: especificaciones y software.

### Almacenamiento persistente

Con AWS CloudShell ella, puedes usar hasta 1 GB de almacenamiento persistente Región de AWS en cada una de ellas sin coste adicional. El almacenamiento persistente se encuentra en tu directorio principal ($HOME) y es privado para ti. A diferencia de los recursos del entorno efímero que se reciclan una vez finalizada cada sesión de shell, los datos del directorio principal persisten entre las sesiones.

Para obtener más información acerca de la retención de datos en el almacenamiento persistente, consulte Almacenamiento persistente.

### Seguridad
ElAWS CloudShell entorno y sus usuarios están protegidos por funciones de seguridad específicas. Esto incluye funciones como la gestión de permisos de IAM, las restricciones de sesión de shell y la función Safe Paste para introducir texto.

### Administración de permisos con IAM

Como administrador, puede conceder y denegar permisos a AWS CloudShell los usuarios mediante políticas de IAM. También puede crear políticas que especifiquen las acciones concretas que los usuarios pueden realizar con el entorno de shell. Para obtener más información, consulte Administrar el AWS CloudShell acceso y el uso con políticas de IAM.

### Administración de sesiones de Shell

Las sesiones inactivas y de larga duración se detienen y se reciclan automáticamente. Para obtener más información, consulte Sesiones de Shell.

### Pegar de forma segura para introducir texto

Safe Paste está habilitado de forma predeterminada. Esta función de seguridad requiere que compruebe que el texto multilínea que desea pegar en el shell no contiene scripts malintencionados. Para obtener más información, consulte Uso de Safe Paste para texto multilínea.

### Opciones de personalización

Puedes personalizar tu AWS CloudShell experiencia según tus preferencias exactas. Por ejemplo, puede cambiar el diseño de la pantalla (varias pestañas), los tamaños del texto mostrado y alternar entre los temas de la interfaz claros y oscuros. Para obtener más información, consulte Personalización de tu AWS CloudShell experiencia.

También puede ampliar su entorno de shell instalando su propio software y modificando los scripts del shell de inicio.

### Restauración de sesión

La función de restauración de sesiones restaura las sesiones que estaba ejecutando en una o varias pestañas del navegador de la CloudShell terminal. Si actualiza o vuelve a abrir las pestañas del navegador cerradas recientemente, esta función reanudará la sesión hasta que se detenga la shell debido a que la sesión está inactiva.

## Referencias
- https://aws.amazon.com/es/cloudshell/