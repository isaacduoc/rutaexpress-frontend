# RutaExpress — Frontend Angular (EP2)

Frontend del sistema académico RutaExpress, desarrollado con Angular 22 y TypeScript para la gestión y seguimiento de envíos.

## Tecnologías

- Angular 22
- TypeScript
- Microsoft Entra ID / MSAL
- AWS API Gateway
- Netlify

## Funcionalidades

- Inicio de sesión mediante Microsoft Entra ID.
- Consulta de servicios disponibles.
- Creación y consulta de envíos.
- Actualización de estados de envíos.
- Integración con las API de RutaExpress.
- Acceso a funcionalidades según el rol del usuario.

## Arquitectura

El frontend se comunica con los microservicios a través de AWS API Gateway y el Backend for Frontend (BFF).

**Flujo:**

Angular → API Gateway → BFF → Microservicios Spring Boot

El BFF valida los tokens JWT y controla los permisos de acceso, incluidos los endpoints exclusivos para administradores.

## Instalación y ejecución local

Desde la carpeta `frontend`:

```bash
npm ci
```

Para iniciar el servidor de desarrollo:

```bash
npx ng serve
```

Abrir en el navegador:

http://localhost:4200

## Compilación de producción

```bash
npm run build
```

Los archivos de producción se generan en:

`dist/frontend-rutaexpress/`

La compilación de producción fue comprobada durante la EP2.

## Despliegue

El frontend está publicado en Netlify:

https://rutaexpress-duoc.netlify.app

El backend se encuentra desplegado en AWS y se accede mediante API Gateway.

## Seguridad

La autenticación utiliza Microsoft Entra ID y tokens JWT.

Las operaciones protegidas requieren autenticación y los permisos correspondientes, validados por el backend.

No almacenar contraseñas, claves privadas ni secretos en el código fuente del frontend.

## Proyecto

Proyecto académico RutaExpress — Entrega Parcial 2 (EP2).

Para conocer la arquitectura completa, RabbitMQ, Oracle y los microservicios, consultar el `README.md` principal del repositorio.