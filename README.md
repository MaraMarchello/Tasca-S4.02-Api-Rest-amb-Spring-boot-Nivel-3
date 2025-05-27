# Tasca-S4.02-Api-Rest-amb-Spring-boot-Nivel-3

# API REST de Gestión de Frutas

## 📄 Descripción - Ejercicio

Este proyecto implementa una API REST para la gestión de frutas utilizando Spring Boot y MongoDB. La aplicación sigue el patrón MVC y permite realizar operaciones CRUD (Crear, Leer, Actualizar y Eliminar) sobre una entidad Fruta.

La entidad Fruta tiene las siguientes propiedades:
- id (int)
- name (String)
- quantityKilos (Integer)

Los endpoints disponibles son:
- POST /fruit/add - Añadir una nueva fruta
- PUT /fruit/update - Actualizar una fruta existente
- DELETE /fruit/delete/{id} - Eliminar una fruta por ID
- GET /fruit/getOne/{id} - Obtener una fruta por ID
- GET /fruit/getAll - Obtener todas las frutas

## 💻 Tecnologías Utilizadas

- Java 21
- Spring Boot 3.4.7
- Spring Data MongoDB
- Lombok
- Maven/Gradle
- MongoDB
- Validation API
- Spring Web
- JUnit (para pruebas)

## 📋 Requisitos

- JDK 21 o superior
- MongoDB 4.4 o superior
- Gradle 8.x
- IDE compatible con Spring Boot (recomendado: IntelliJ IDEA o Spring Tool Suite)
- Postman (para pruebas de API)

## 🛠️ Instalación

1. Clonar el repositorio:
```bash
git clone https://github.com/MaraMarchello/Tasca-S4.02-Api-Rest-amb-Spring-boot-Nivel-3
```

2. Navegar al directorio del proyecto:
```bash
cd S04T02N03
```

3. Compilar el proyecto:
```bash
./gradlew build
```

4. Asegurarse de que MongoDB está en ejecución en localhost:27017

## ▶️ Implementación

1. Ejecutar la aplicación:
```bash
./gradlew bootRun
```

2. La aplicación estará disponible en:
```
http://localhost:8080
```

3. Probar los endpoints usando Postman:

Ejemplo de petición POST para crear una fruta:
```json
POST http://localhost:8080/fruit/add
Content-Type: application/json

{
    "id": 1,
    "name": "Manzana",
    "quantityKilos": 100
}
```

## 🌐 Despliegue

1. Generar el archivo JAR:
```bash
./gradlew build
```

2. El archivo JAR se generará en:
```
build/libs/S04T02N03-0.0.1-SNAPSHOT.jar
```

3. Ejecutar en producción:
```bash
java -jar build/libs/S04T02N03-0.0.1-SNAPSHOT.jar
```

Configuración de MongoDB para producción en application.properties:
```properties
spring.data.mongodb.host=your-mongodb-host
spring.data.mongodb.port=27017
spring.data.mongodb.database=fruitsdb
```

## 🤝 Contribución

1. Hacer un Fork del proyecto
2. Crear una rama para tu funcionalidad:
```bash
git checkout -b feature/nueva-funcionalidad
```
3. Commit de los cambios:
```bash
git commit -m 'Añadir nueva funcionalidad'
```
4. Push a la rama:
```bash
git push origin feature/nueva-funcionalidad
```
5. Crear un Pull Request

### Guías de Contribución
- Seguir las convenciones de código de Java
- Documentar nuevas funcionalidades
- Añadir pruebas unitarias para nuevas funcionalidades
- Actualizar README.md si es necesario

## 📝 Notas Adicionales

- La aplicación implementa un manejador global de excepciones
- Incluye validación de datos de entrada
- Utiliza ResponseEntity para manejar las respuestas HTTP
- Implementa el patrón Builder con Lombok para la creación de objetos 
