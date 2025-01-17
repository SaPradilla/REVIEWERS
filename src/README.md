REVIEWERS: Review Platform
Este proyecto es una plataforma de reseñas donde los usuarios pueden registrarse, escribir reseñas sobre diferentes negocios, votar sobre reseñas útiles y acumular puntos para ganar recompensas. También incluye funcionalidades para que los administradores gestionen usuarios y negocios dentro del sistema.

Tecnologías Utilizadas
Node.js con Express: Framework para construir el backend.
Prisma ORM: Para gestionar la base de datos relacional (MySQL).
MySQL: Base de datos relacional utilizada.
Bcrypt: Para el manejo seguro de contraseñas (hashing).
Nodemailer: Para el envío de correos de confirmación para registros.
Git: Sistema de control de versiones.
Instalación
1. Clonar el repositorio:
git clone https://github.com/Program0017/REVIEWERS.git

cd REVIEWERS
2. Instalar las dependencias:
Asegúrate de tener Node.js instalado y luego ejecuta:
npm install


3. Configurar la base de datos:
Asegúrate de que MySQL esté en funcionamiento y crea una base de datos reviewers llamada reviewers antes de migrar el esquema.
Configura la URL de conexión en el archivo .env. Asegúrate de tener el archivo .env en la raíz del proyecto con el siguiente contenido:
DATABASE_URL="mysql://user:password@localhost:3306/reviewers_db"
Reemplaza "user" y "password" con tus credenciales de MySQL.

4. Migrar el esquema de la base de datos:
Para migrar el esquema de la base de datos usando Prisma, ejecuta el siguiente comando:
npx prisma migrate dev --name init
Si necesitas hacer otra migración, por ejemplo, después de añadir cambios al modelo, utiliza:

npx prisma migrate dev --name <nombre-de-tu-migracion>
Ejemplo de migración adicional:



6. Iniciar el servidor:
Después de configurar la base de datos y las migraciones, inicia el servidor con el siguiente comando:
node server.js

Endpoints de la API
Aquí tienes una lista de los endpoints clave de la API:

POST /register: Registrar un nuevo usuario.
GET /users: Listar todos los usuarios (solo para administradores).
POST /reviews: Enviar una reseña para un negocio.
GET /businesses: Listar todos los negocios.
POST /votes: Votar sobre una reseña.

Características
Registro de usuarios con nombres de usuario y correos electrónicos únicos.
Hashing de contraseñas para una autenticación segura.
Confirmación por correo electrónico para la activación de la cuenta.
Envío de reseñas para negocios con imágenes opcionales.
Sistema de votación para marcar reseñas como útiles o no.
Funcionalidades de administración para gestionar usuarios y negocios.
Contribuciones
¡Las contribuciones son bienvenidas! Por favor, crea un pull request para cualquier mejora o corrección de errores.

Licencia
Este proyecto está licenciado bajo la Licencia MIT.

Contacto
Para consultas, por favor contacta con nosotros.

