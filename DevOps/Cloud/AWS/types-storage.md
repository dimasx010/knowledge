# Types Storage

Los servicios de almacenamiento de AWS se agrupan en tres categorías: almacenamiento de bloque, almacenamiento de archivos y almacenamiento de objetos.

## Almacenamiento de archivos

Puede que esté familiarizado con el almacenamiento de archivos si ha interactuado con los sistemas de almacenamiento de archivos, como Windows File Explorer o Finder en macOS. Los archivos se organizan en una jerarquía de árbol que consta de carpetas y subcarpetas. Por ejemplo, si tiene cientos de fotos de gatos en su laptop, tal vez quiera crear una carpeta llamada “Fotos de gatos” y colocar las imágenes en esa carpeta para organizarlas. Dado que sabe que estas imágenes se utilizarán en una aplicación, es posible que desee colocar la carpeta Fotos de gatos dentro de otra carpeta denominada “Archivos de la aplicación”.

Cada archivo tiene metadatos, como el nombre del archivo, el tamaño del archivo y la fecha en que se creó el archivo. El archivo también tiene una ruta de acceso, por ejemplo, computer/Application_files/Cat_photos/cats-03.png. Cuando tenga que recuperar un archivo, el sistema puede utilizar la ruta para encontrarlo en la jerarquía de archivos.

El almacenamiento de archivos es ideal cuando necesita el acceso centralizado a los archivos que varios equipos host deben compartir y administrar fácilmente. Normalmente, este almacenamiento se monta en varios hosts y requiere el bloqueo de archivos y la integración en los protocolos de comunicación del sistema de archivos existentes.

Los casos de uso comunes para el almacenamiento de archivos incluyen los siguientes:

- Grandes repositorios de contenido
- Entornos de desarrollo
- Directorios de inicio de usuario

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/ab917891-c183-4d48-a074-e6ea0197b68a">
</p>

## Almacenamiento de bloque

Si bien el almacenamiento de archivos trata los archivos como una unidad singular, el almacenamiento de bloque divide los archivos en fragmentos de datos de tamaño fijo llamados “bloques” que tienen sus propias direcciones. Dado que cada bloque es direccionable, los bloques se pueden recuperar de forma eficiente.

Cuando se solicitan datos, el sistema de almacenamiento utiliza las direcciones para organizar los bloques en el orden correcto y formar un archivo completo para presentarlo al solicitante. Fuera de la dirección, no hay metadatos adicionales asociados a cada bloque. Por lo tanto, cuando quiera cambiar un carácter de un archivo, simplemente cambia el bloque o el fragmento del archivo que contiene el carácter. Esta facilidad de acceso es la razón por la que las soluciones de almacenamiento en bloque son rápidas y utilizan menos banda ancha.

Dado que el almacenamiento en bloque está optimizado para operaciones de baja latencia, es una opción típica de almacenamiento para las cargas de trabajo empresariales de alto rendimiento, como los sistemas de planificación de recursos empresariales (ERP) o las bases de datos, que requieren almacenamiento de baja latencia.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/b1d64541-de37-4b9c-badb-e066039935fe">
</p>


## ​Almacenamiento de objetos

Los objetos, al igual que los archivos, se tratan como una única unidad de datos cuando se almacenan. Sin embargo, a diferencia del almacenamiento de archivos, estos objetos se almacenan en una estructura plana en lugar de en una jerarquía. Cada objeto es un archivo con un identificador único. Este identificador, junto con cualquiera de los metadatos adicionales, se empaqueta con los datos y se almacena.

Cambiar un solo carácter de un objeto es más difícil que con el almacenamiento de bloque. Cuando quiere cambiar un carácter de un archivo, debe actualizarse todo el archivo.

Con el almacenamiento de objetos, puede almacenar casi cualquier tipo de datos, y no hay límite para el número de objetos almacenados, lo que lo hace fácilmente escalable. El almacenamiento de objetos suele ser útil cuando se almacenan grandes conjuntos de datos; archivos no estructurados, como activos multimedia; y recursos estáticos, como fotos.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2b3c9aa4-d401-4259-aabe-1a9a52357767">
</p>

