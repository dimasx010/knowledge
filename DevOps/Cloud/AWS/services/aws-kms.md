# AWS Key Management Service

AWS Key Management Service (AWS KMS) es un servicio administrado que le permite crear y controlar fácilmente las claves de cifrado que se utilizan para proteger sus datos. AWS KMS utiliza módulos de seguridad de hardware (HSM) para proteger y validar su AWS KMS keys según el Programa de validación de módulos criptográficos FIPS 140-2. Las regiones de China (Beijing) y China (Ningxia) no admiten el programa de validación del módulo criptográfico FIPS 140-2. AWS KMSutiliza HSM certificados por OSCCA para proteger las claves de KMS en las regiones de China

<p align="center">
  <img src="https://github.com/dimasx010/knowledge/assets/105082657/9a17c561-772a-43b4-952b-ffd3599e7dee">
</p>

AWS KMS está integrado con la mayoría de los demás servicios de AWS que cifran sus datos. AWS KMS también está integrado con AWS CloudTrail para registrar el uso de sus claves KMS para las necesidades de auditoría, regulación y cumplimiento.

Puede utilizar la API AWS KMS para crear y administrar claves KMS y funciones especiales, como almacenes de claves personalizadas y utilizar claves KMS en operaciones criptográficas. 

## References
- https://docs.aws.amazon.com/es_es/kms/latest/developerguide/overview.html
