# Hadolinl

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/faa25d16-f230-4ec7-aca6-75cebe3e7f9b">
</p>

Hadolint es un filtro de Dockerfile que puede detectar problemas comunes por usted. Utiliza un árbol de sintaxis abstracta (AST) para analizar su Dockerfile contra conjuntos de reglas predefinidos. Hadolint también incorpora ShellCheck para que pueda filtrar los scripts de shell en su Dockerfile. RUN instrucciones también.
Hadolint tiene docenas de reglas integradas que verifican problemas comunes de configuración y seguridad. El linter tiene como objetivo hacer que sus Dockerfiles cumplan con las mejores prácticas de creación de imágenes sugeridas por Docker.

Las comprobaciones incluidas cubren el uso de usuarios finales no root, haciendo referencia a una ruta relativa en un WORKDIR declaración, agregando múltiples HEALTHCHECK instrucciones, y no usar etiquetas y versiones fijadas explícitamente. Como Hadolint también hereda el conjunto de reglas de ShellCheck, surgirán problemas comunes de secuencias de comandos de Bash que esa herramienta también identifica.

Las reglas se identifican como números con el prefijo HL o SC. HL las reglas son parte de Hadolint mientras que SC las entradas provienen de ShellCheck. A cada verificación se le asigna una gravedad desde Error hasta Información. Si obtiene errores en los resultados de su análisis, esos deberían ser los primeros problemas que resuelva.

## References
- https://alexandre-vazquez.com/hadolint-best-practices-for-your-dockerfiles/
- https://diarioinforme.com/como-usar-hadolint-para-filtrar-sus-dockerfiles/#google_vignette​
