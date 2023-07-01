#  Editor de texto VI

​Vi es un editor de texto que se encuentra disponible en todas las distribuciones GNU/Linux y en gran parte de Unix. El editor Vi maneja el texto entero de un archivo en memoria, y proporciona muchas otras funcionalidades que lo hacen convertirse en uno de los editores de texto más usados por los administradores. Además, en ciertas situaciones de emergencia, este es el único editor que tendremos disponible.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/a9f49b2f-7890-404f-b3f6-1e4d2a8bf3da">
</p>

## Modos de operación en editor Vi

- Comando: es el modo en el que encontrarás al editor cada vez que se inicia. Este modo acepta comandos en forma de letras, mueve el cursor, ejecuta comandos de salidas de texto, permite guardar cambios o salir de el editor, entre otros.

- Edición o insert de texto: permite añadir texto al fichero, es decir, cualquier carácter que introduzcamos será insertado en el documento (con la tecla esc como excepción)

- Ex o última línea: usado para escribir comandos en la última línea al final de la pantalla. Es precedido por : y permite la manipulación de ficheros.

## Comandos del editor de texto Vi

Algunos de los comandos del editor Vi se listarán a continuación:

### Para iniciar en el editor Vi:

- vi: abre el programa sin ningún archivo.
- vi fichero: edita el fichero si existe, y si no, lo crea.
- vi fichero1 fichero2: edita varios archivos.
    :next o :n para pasar al siguiente archivo.
    :prev o :N para ir al archivo previo.
- vi + [número fichero] : edita el fichero iniciando en la línea indicada.
- vi+/patrón fichero: edita el fichero iniciando en la primera vez que encuentre el patrón.

### Demás comandos del editor Vi:

- i para insertar texto a la izquierda del cursor.
- a para insertar texto a la derecha del cursor.
- I se encarga de insertar texto al inicio de la línea.
- A es el encargado de insertar texto al final de la línea.
- ESC vuelve al modo comando.
- X es el comando que borra el carácter bajo el cursor.
- dd para borrar la línea actual.
- dw borra la palabra actual.
- h o flecha izquierda moverá el cursor hacia la izquierda.
- j o flecha abajo moverá el cursor a la línea de abajo.
- k o flecha arriba mueve el cursor a la línea de arriba.
- l o flecha derecha mueve el cursor a la derecha.
- :w guarda los cambios.
- :q para salir del editor.

Además, el modo comando contiene ciertos multiplicadores que permite ejecutar un comando tantas veces como se le indique en el editor de texto Vi, así por ejemplo:

- 5Y copia cinco líneas.
- 10dd borra diez líneas.
- 3dw borra 3 palabras.
- 8j mueve el cursor 8 líneas abajo.

Respecto al movimiento del cursor en el modo comando del editor de texto Vi, tenemos:

- Flechas: mover en distintas direcciones.
- $ : mueve al inicio o al final de la línea.
- G : última línea.
- xG : mueve el cursor a la línea x.
- xl : mueve el cursor al carácter x de la línea.

En cuanto a los movimientos de pantalla, tenemos en el editor de texto Vi:

- Ctrl+ f : una pantalla adelante.
- Ctrl+ b : una pantalla atrás.
- Ctrl+ d : media pantalla adelante.
- Ctrl+ u : media pantalla atrás.

## Referencias

- https://keepcoding.io/blog/como-funciona-el-editor-de-texto-vi/