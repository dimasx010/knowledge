# User-data - Amazon EC2

Básicamente User-data nos permite ejecutar comandos en la instancia de linux (EC2) durante su lanzamiento. 

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/9437d8f0-923e-44ef-94a8-b7c7f173faa9">
</p>

Cuando se lanza una instancia en Amazon EC2, tiene la opción de transmitir los datos de usuario a la instancia que se pueden utilizar para realizar tareas de configuración automáticas comunes e incluso ejecutar scripts después de que se inicie la instancia. Puede transferir dos tipos de datos de usuario a Amazon EC2: scripts de intérprete de comandos y directivas cloud-init. También puede pasar estos datos en el asistente de lanzamiento de instancias como texto sin formato, como archivo (esto resulta útil para lanzar instancias con las herramientas de la línea de comandos) o como texto codificado en base64 (para llamadas a la API). Por ejemplo podemos instalar una infra LAMP en la mencionada instancia una vez que la iniciemos su lanzamiento. 

## Referencias
- https://docs.aws.amazon.com/es_es/AWSEC2/latest/UserGuide/user-data.html