# Proceso de Despliegue - PokeDex

## 1. Construcción del proyecto

Se realizó la construcción de la aplicación Angular utilizando el siguiente comando:

npx ng build --base-href ./

Este comando generó la carpeta de distribución:

dist/pokedex-angular

---

## 2. Problemas encontrados y soluciones

### Error 1: comando ng no reconocido

Error presentado:

"ng" no se reconoce como un comando interno o externo

Solución:

Se utilizó el comando:

npx ng build --base-href ./

---

### Error 2: aplicación en blanco

Al desplegar la aplicación inicialmente, la página aparecía en blanco.

Solución:

Se identificó que se estaban subiendo rutas incorrectas. Se corrigió subiendo únicamente el contenido interno de:

dist/pokedex-angular

---

### Error 3: fallo en GitHub Actions

Error presentado:

No credentials found. Add an Azure login action

Solución:

1. Se descargó el archivo de perfil de publicación desde Azure.
2. Se creó un secret en GitHub llamado:

AZURE_WEBAPP_PUBLISH_PROFILE

3. Se configuró correctamente el workflow para autenticación y despliegue.

   <img width="1046" height="422" alt="image" src="https://github.com/user-attachments/assets/004ae6e2-ce5c-40e0-9d83-58a74e6ba406" />


---

## 3. Configuración de CI/CD

Se utilizó GitHub Actions para automatizar el despliegue.

Cada vez que se realiza un commit en la rama principal, el sistema:

- Construye el paquete
- Se conecta a Azure
- Despliega automáticamente la aplicación

---

## 4. Implementación de seguridad

Se creó un archivo `web.config` en la raíz del proyecto con los encabezados HTTP necesarios para mejorar la seguridad.

Encabezados implementados:

- X-Frame-Options: DENY
- X-Content-Type-Options: nosniff
- Referrer-Policy: no-referrer
- Strict-Transport-Security
- Content-Security-Policy

---

## 5. Validación de seguridad

Se realizó un escaneo utilizando la herramienta:

https://securityheaders.com/

Resultado obtenido:

Calificación A

---

## 6. Estado final

- Aplicación desplegada correctamente en la nube
- Acceso público mediante URL
- Despliegue automático funcionando
- Encabezados de seguridad implementados
- Evaluación de seguridad aprobada
