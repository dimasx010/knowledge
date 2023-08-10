# AWS Price API

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/cc796edd-43f4-4989-b261-fe39f94176ad">
</p>

AWS ofrece dos API que puede utilizar para consultar precios:

- Con la API masiva de lista de precios de AWS, puede consultar los precios de servicios de AWS de forma masiva. La API devuelve un archivo JSON o CSV. La API masiva retiene todas las versiones históricas de la lista de precios.

- Con la API de consulta de lista de precios de AWS, se puede consultar información específica sobre servicios, productos y precios de AWS mediante un AWS SDK o la AWS CLI. Esta API puede recuperar información sobre determinados productos o precios, en lugar de recuperar precios de forma masiva. Esto permite obtener información de precios en entornos que tal vez no puedan procesar una lista de precios masiva, como en aplicaciones móviles o basadas en un navegador web. Por ejemplo, puede utilizar la API de consulta para obtener información sobre los precios de instancias de Amazon EC2 con 64 CPU, 256 GiB de memoria y SQL Server Enterprise preinstalado en la región de Asia Pacífico (Mumbai). La API de consulta ofrece los precios actuales y no retiene los precios históricos.


## References
- https://docs.aws.amazon.com/es_es/awsaccountbilling/latest/aboutv2/price-changes.html