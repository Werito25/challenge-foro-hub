# ForoHub

## Descripción
ForoHub es una API REST desarrollada con Spring Boot que permite gestionar un foro en línea. Los usuarios pueden realizar operaciones como crear, leer, actualizar y eliminar temas y respuestas, además de buscar información específica. La aplicación utiliza una base de datos MySQL para almacenar los datos del foro y está protegida con autenticación.

---

## Tecnologías Utilizadas
- **Lenguaje de programación**: Java 17
- **Framework**: Spring Boot 3.4.1
- **Base de datos**: MySQL Workbench 8.0
- **Herramientas de desarrollo**:
  - IntelliJ IDEA
  - Insomnia (para pruebas de la API)
- **Gestor de dependencias**: Maven

---

## Características
- CRUD (Create, Read, Update, Delete) completo para la gestión de temas y respuestas del foro.
- Autenticación con Spring Security.
- Configuración de base de datos utilizando HikariCP.
- Manejo de excepciones personalizado para errores de validación y acceso.

---

## Endpoints Principales

### Temas
- **GET /temas**: Obtiene todos los temas.
- **POST /temas**: Crea un nuevo tema.
- **PUT /temas/{id}**: Actualiza un tema existente.
- **DELETE /temas/{id}**: Elimina un tema por ID.

### Respuestas
- **GET /respuestas**: Obtiene todas las respuestas.
- **POST /respuestas**: Crea una nueva respuesta.
- **PUT /respuestas/{id}**: Actualiza una respuesta existente.
- **DELETE /respuestas/{id}**: Elimina una respuesta por ID.

### Autenticación
- Configurada para proteger los endpoints mediante Basic Auth o un sistema personalizado de usuarios.

---

## Instalación y Configuración

### Prerrequisitos
1. **Java**: Asegúrate de tener instalada la versión 21.
2. **Maven**: Para gestionar las dependencias del proyecto.
3. **MySQL**: Base de datos para la aplicación (versión 8.0 o superior).

### Configuración Inicial
1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/challenge-foro-hub.git  
   ```

2. Configura el archivo `application.properties` para conectar con tu base de datos MySQL:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/nombredebasededatos
spring.datasource.username=tu_usuario
spring.datasource.password=*****
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
spring.flyway.baseline-on-migrate=true


server.error.include-stacktrace=never


api.security.secret=${JWT_SECRET}
   ```

3. Ejecuta el siguiente comando para compilar y ejecutar la aplicación:
   ```bash
   mvn spring-boot:run
   ```

---

## Uso

### Probar la API
Utiliza herramientas como **Insomnia** o **Postman** para interactuar con los endpoints de la API. Asegúrate de incluir las credenciales si el endpoint está protegido.

### Credenciales por defecto
En modo de desarrollo, puedes usar las siguientes credenciales:
- **Usuario**: `user`
- **Contraseña**: Generada automáticamente (consulta los logs de la aplicación).

---

## Contribuciones
Si deseas contribuir a este proyecto:
1. Haz un fork del repositorio.
2. Crea una rama para tu nueva característica o corrección de errores.
3. Envía un Pull Request detallando tus cambios.

---

## Licencia
Este proyecto está bajo la licencia JML.


