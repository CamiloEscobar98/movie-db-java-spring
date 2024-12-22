# Movies-DB Backend

## Descripción
Movies-DB es un proyecto de aprendizaje desarrollado en Java con Spring Boot que implementa un sistema de gestión para el alquiler de películas. Este repositorio corresponde al Backend del proyecto, encargado de gestionar la lógica de negocio, la comunicación con la base de datos y la exposición de servicios a través de una API REST.

---

## Características
- Gestión de usuarios y autenticación.
- Administración de películas disponibles para alquiler.
- Control de alquileres, devoluciones y disponibilidad.
- Integración con bases de datos relacionales.
- Documentación de la API con Swagger/OpenAPI.

---

## Tecnologías Utilizadas
- **Java**: Lenguaje de programación principal.
- **Spring Boot**: Framework para el desarrollo del Backend.
- **Spring Data JPA**: Gestión de persistencia y acceso a la base de datos.
- **MySQL**: Base de datos relacional utilizada.
- **Spring Security**: Autenticación y autorización de usuarios.
- **Swagger/OpenAPI**: Documentación interactiva de la API REST.
- **Lombok**: Reducción de código repetitivo.

---

## Requisitos Previos
1. Tener instalado Java 17 o superior.
2. Contar con un entorno de desarrollo como IntelliJ IDEA o Eclipse.
3. Tener configurado MySQL en tu máquina local o en un servidor.
4. Administrador de dependencias como Maven o Gradle.

---

## Instalación y Configuración
1. Clonar este repositorio:
    ```bash
    git clone <URL_DEL_REPOSITORIO>
    ```

2. Configurar el archivo `application.properties` o `application.yml` en el directorio `src/main/resources` con los datos de conexión a tu base de datos:
    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/movies_db
    spring.datasource.username=usuario
    spring.datasource.password=contraseña

    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect
    ```

3. Ejecutar el proyecto:
    ```bash
    mvn spring-boot:run
    ```

---

## Estructura del Proyecto
- **Controller**: Maneja las solicitudes HTTP y delega las operaciones al servicio correspondiente.
- **Service**: Contiene la lógica de negocio del sistema.
- **Repository**: Acceso a la base de datos mediante Spring Data JPA.
- **Entity**: Define las entidades del sistema y su mapeo a la base de datos.
- **DTO (Data Transfer Object)**: Facilita la transferencia de datos entre capas.

---

## Endpoints Iniciales
A continuación, algunos de los endpoints básicos que se implementarán:

### Usuarios
- **POST /api/users/register**: Registro de nuevos usuarios.
- **POST /api/users/login**: Autenticación de usuarios.

### Películas
- **GET /api/movies**: Listado de películas disponibles.
- **POST /api/movies**: Crear una nueva película (requiere permisos).

### Alquileres
- **POST /api/rentals**: Registrar un alquiler de película.
- **POST /api/returns**: Registrar la devolución de una película.

---

## Próximos Pasos
- Agregar validaciones y manejo de errores personalizados.
- Ampliar el sistema de roles y permisos.
- Implementar pruebas unitarias e integración.
- Crear un sistema de recomendaciones basado en las preferencias de los usuarios.

---

## Contribución
Este proyecto está diseñado como una herramienta de aprendizaje. Si deseas contribuir, por favor sigue las normas básicas de estilo de código y añade comentarios donde sea necesario.

---

## Licencia
Este proyecto es de uso libre para fines educativos.
