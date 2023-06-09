# Helm

## General

Helm es ampliamente conocido como "el gestor de paquetes para Kubernetes". Aunque se presenta así, su alcance va mucho más allá del de un simple gestor de paquetes. Sin embargo, empecemos por el principio.

Helm es un proyecto de código abierto que fue creado originalmente por DeisLabs y donado a CNCF, que ahora lo mantiene. El objetivo original de Helm era proporcionar a los usuarios una forma mejor de gestionar todos los archivos YAML de Kubernetes que creamos en los proyectos de Kubernetes.

El camino que Helm tomó para resolver este problema fue crear Helm Charts. Cada gráfico es un paquete con uno o más manifiestos de Kubernetes: un gráfico puede tener gráficos hijos y gráficos dependientes.

Esto significa que Helm instala todo el árbol de dependencias de un proyecto si ejecuta el comando install para el gráfico de nivel superior. Sólo tiene que ejecutar un único comando para instalar toda su aplicación, en lugar de listar los ficheros a instalar mediante kubectl.

Charts también te permite versionar tus archivos de manifiesto, al igual que hacemos con Node.js o cualquier otro paquete. Esto te permite instalar versiones específicas de gráficos, lo que significa mantener configuraciones específicas para tu infraestructura en forma de código.

Helm también mantiene un historial de versiones de todas las cartas desplegadas, por lo que puede volver a una versión anterior si algo va mal.

Helm soporta Kubernetes de forma nativa, lo que significa que no tienes que escribir ningún archivo de sintaxis complejo ni nada para empezar a usar Helm. Solo tienes que soltar tus archivos de plantilla en un nuevo gráfico y listo.

Pero, ¿por qué deberíamos utilizarlo? La gestión de los manifiestos de aplicación puede hacerse fácilmente con unas pocas combinaciones de comandos.