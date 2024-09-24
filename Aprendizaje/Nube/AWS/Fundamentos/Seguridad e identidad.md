#Cloud #AWS #Fundamentos

[[Daily/2024-04-15.md|2024-04-15]]

```table-of-contents
title: 
style: nestedList # TOC style (nestedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
includeLinks: true # Make headings clickable
debugInConsole: false # Print debug info in Obsidian console
```
Uno de los aspectos más importantes al trasladar aplicaciones en la nube es la **seguridad**. Es crucial que nuestros datos estén protegidos contra amenazas para así permitir que los usuarios accedan a nuestro sistema y encuentren solo los recursos que necesitan.

# Servicios de protección de datos

A continuación, conocerás algunos servicios de protección de AWS y sus funciones para mover nuestras plataformas en la nube:

- **Amazon Macie:** descubre y protege datos sensibles
- **AWS Key Management Service:** almacena y administra claves de cifrado
- **AWS CloudHSM:** proporciona almacenamiento de claves basado en hardware
- **AWS Certificate Manager:** provee, administra e implementa certificados SSL/TLS
- **AWS Secrets Manager:** traslada, gestiona y recupera datos (contraseñas, por ejemplo)

# Servicios de protección de la infraestructura

Es fundamental que cuides de la infraestructura de tu sitio web y AWS ofrece los siguientes servicios de seguridad:

- **AWS Shield:** protege contra ataques de Denegación de Servicio (DDOS)
- **AWS Web Aplication Firewall (WAF):** filtra el tráfico de sitios web maliciosos
- **AWS Firewall Manager:** administra las reglas del firewall de forma centralizada

# Servicios de detección de amenazas

En todo momento nuestra plataforma está expuesta a grandes amenazas y por eso AWS desarrolló los siguientes servicios:

- **Amazon GuarDuty:** detecta automáticamente las amenazas
- **Amazon Inspector:** analiza la seguridad de la aplicación
- **Amazon Config:** registra y evalúa configuraciones de nuestros recursos
- **Amazon CloudTrail:** rastrea la actividad del usuario y el uso de las API que ocupamos en nuestra cuenta.

# Servicios de gestión de identidad

Por último, existen distintas herramientas de gestión de identidad que provee AWS:

- **AWS Identity and Access Management (IAM):** administra de forma segura el acceso a una cuenta, servicios y recursos
- **AWS Inicio de sesión único:** implementa el inicio de sesión único (Single Sign On/SSO)
- **Amazon Cognito:** permite a los usuarios administrar la identidad dentro de las aplicaciones
- **AWS Servicio de Directorio:** implementa y administra un Active Directory service
- **AWS Organizaciones:** funciona para gobernar y administrar de distintas cuentas de AWS de forma centralizada