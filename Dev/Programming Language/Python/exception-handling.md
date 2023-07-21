# Python - Manejo de excepciones

Los errores de ejecución son llamados comúnmente excepciones y por eso de ahora en más utilizaremos ese nombre. Durante la ejecución de un programa, si dentro de una función surge una excepción y la función no la maneja, la excepción se propaga hacia la función que la invocó, si esta otra tampoco la maneja, la excepción continua propagándose hasta llegar a la función inicial del programa y si esta tampoco la maneja se interrumpe la ejecución del programa. Veamos entonces como manejar excepciones.

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/4fc53d3e-6e14-48d0-8bf8-b4ee6c7b929c">
</p>

Para el manejo de excepciones los lenguajes proveen ciertas palabras reservadas, que nos permiten manejar las excepciones que puedan surgir y tomar acciones de recuperación para evitar la interrupción del programa o, al menos, para realizar algunas acciones adicionales antes de interrumpir el programa.

En el caso de Python, el manejo de excepciones se hace mediante los bloques que utilizan las sentencias try, except y finally.

Dentro del bloque try se ubica todo el código que pueda llegar a levantar una excepción, se utiliza el término levantar para referirse a la acción de generar una excepción.

A continuación se ubica el bloque except, que se encarga de capturar la excepción y nos da la oportunidad de procesarla 

```python
>>> try:
...     cociente = dividendo / divisor
... except:
...     print "No se permite la división por cero"
...
```

Dado que dentro de un mismo bloque try pueden producirse excepciones de distinto tipo, es posible utilizar varios bloques except, cada uno para capturar un tipo distinto de excepción.

Esto se hace especificando a continuación de la sentencia except el nombre de la excepción que se pretende capturar. Un mismo bloque except puede atrapar varios tipos de excepciones, lo cual se hace especificando los nombres de la excepciones separados por comas a continuación de la palabra except. Es importante destacar que si bien luego de un bloque try puede haber varios bloques except, se ejecutará, a lo sumo, uno de ellos.

```python
try:
    # aquí ponemos el código que puede lanzar excepciones
except IOError:
    # entrará aquí en caso que se haya producido
    # una excepción IOError
except ZeroDivisionError:
    # entrará aquí en caso que se haya producido
    # una excepción ZeroDivisionError
except:
    # entrará aquí en caso que se haya producido
    # una excepción que no corresponda a ninguno
    # de los tipos especificados en los except previos
```

Ahora si deseamos saber que excepción se esta produciendo lo ideal sería utilizar la siguiente rutina: 

```python
try:
    # aquí ponemos el código que puede lanzar excepciones
except Exception as err:
    print(f"Unexpected {err=}, {type(err)=}")
    raise
```

## Referencias: 

- https://docs.python.org/es/3/tutorial/errors.html
- https://uniwebsidad.com/libros/algoritmos-python/capitulo-12/excepciones