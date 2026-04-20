# PokeDex - Despliegue en la Nube

## Descripción

Este proyecto consiste en el despliegue de una aplicación web estática denominada PokeDex, la cual permite visualizar información de diferentes especies de Pokémon.

La aplicación fue desarrollada en Angular y posteriormente desplegada en la nube utilizando Microsoft Azure App Service, aplicando buenas prácticas de despliegue y seguridad web.

---

## URL de la aplicación

https://app-listrace-web-prod-jdrc-pokedex-adafbhfqcxayddd5.eastus2-01.azurewebsites.net/

<img width="1850" height="932" alt="image" src="https://github.com/user-attachments/assets/287fa80c-9bd4-4099-9be9-132b326956d4" />


---

## Tecnologías utilizadas

- Angular
- HTML, CSS, JavaScript
- Microsoft Azure App Service
- GitHub Actions (CI/CD)

---

## Proceso general

1. Creación de cuenta en Azure for Students.
2. Creación del recurso App Service.

<img width="1404" height="887" alt="image" src="https://github.com/user-attachments/assets/1d18f823-03f3-4d4b-b336-cb83b4006f0c" />


3. Construcción del proyecto Angular para producción.
4. Subida del código al repositorio en GitHub.
5. Configuración de despliegue automático con GitHub Actions.
6. Configuración de encabezados HTTP de seguridad.

---

## Seguridad

Se implementaron encabezados HTTP de seguridad mediante un archivo `web.config`, incluyendo:

- X-Frame-Options
- X-Content-Type-Options
- Referrer-Policy
- Strict-Transport-Security
- Content-Security-Policy

La aplicación fue evaluada en securityheaders.com obteniendo una calificación:

A

---

## Evidencia

Se adjunta captura del resultado del escaneo de seguridad realizado en securityheaders.com.

---

## Reflexión

Este proyecto permitió comprender la importancia del despliegue seguro de aplicaciones web en la nube, así como la configuración de encabezados HTTP para mitigar vulnerabilidades comunes como ataques XSS, clickjacking y exposición de información sensible.
