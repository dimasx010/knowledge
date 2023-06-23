# HashiCorp Configuration Language

HashiCorp Configuration Language (HCL) es un lenguaje de configuración único. Fue diseñado para usarse con las herramientas de HashiCorp, especialmente Terraform, pero HCL se ha expandido como un lenguaje de configuración más general. Es visualmente similar a JSON con estructuras de datos y capacidades adicionales integradas.


<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/2ba1a2a0-1f7a-4094-a00a-8c30909847fb">
</p>

HCL consta de tres sublenguajes:

- Estructural
- Expresión
- Plantillas

Cuando se combinan, los sublenguajes forman un archivo de configuración HCL bien estructurado. Esta estructura ayuda a describir con precisión y facilidad las configuraciones ambientales necesarias para la herramienta Terraform.

Recientemente, HCL ha dejado de usar la versión 1 del lenguaje a favor de la versión 2.HCL2 es una combinación de HCL y HashiCorp Interpolation Language (HIL). HIL agrega interpolación de cadenas y una mayor capacidad para usar funciones en declaraciones de variables.

HCL también se puede usar con otras herramientas además de Terraform. Con el tiempo, diferentes analizadores han estado disponibles, como Go, Java y Python. En esta publicación, analizo cómo comenzar a usar HCL y qué herramientas aprovechan sus características únicas.

## Referencias
- https://recluit.com/que-es-hcl/
