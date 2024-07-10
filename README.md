# Sistema de Autenticación JWT con Expiración de Tokens

Este proyecto implementa un sistema de autenticación utilizando JSON Web Tokens (JWT) con Express.js. Incluye funcionalidad de expiración de tokens para mejorar la seguridad.

## Características

- Registro de usuarios
- Login con generación de tokens JWT
- Verificación de tokens
- Expiración de tokens después de 30 minutos

## Instalación

1. Clona el repositorio
2. Ejecuta `npm install` para instalar las dependencias
3. Crea un archivo `.env` en la raíz del proyecto con las siguientes variables:
    JWT_SECRET=tu_secreto_muy_seguro
    PORT=3000
4. Ejecuta `node app.js` para iniciar el servidor

## Endpoints

- POST /register: Registra un nuevo usuario
- POST /login: Autentica un usuario y devuelve un token JWT
- GET /verify: Verifica la validez de un token JWT

## Consideraciones de Seguridad

- Los tokens expiran después de 30 minutos para limitar el tiempo de acceso.
- Las contraseñas se almacenan hasheadas utilizando bcrypt.
- Se utiliza un secreto JWT almacenado en variables de entorno.
- Se verifica la validez y expiración del token en cada solicitud autenticada.

## Pruebas

Se recomienda usar Thunder Client o una herramienta similar para probar los endpoints. Asegúrese de incluir el token JWT en el encabezado de autorización para las rutas protegidas.