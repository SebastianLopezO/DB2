# Portafolio de Bases de Datos II (NoSQL)

Este repositorio documenta el recorrido de aprendizaje en la asignatura **Bases de Datos II**, enfocado principalmente en bases de datos no relacionales (**NoSQL**), modelado de documentos, agregaciones complejas e integración de persistencia en arquitecturas modernas y contenerizadas.

**Autor:** Sebastián López Osorno
**Tecnología Base:** MongoDB

-----

## 🏗️ Arquitectura del Portafolio

El repositorio se divide en hitos de aprendizaje que van desde la consola de comandos hasta el despliegue de aplicaciones distribuidas.

### 1\. 🛍️ FashionLine: Sistema Full Stack (Parcial 2)

**Ubicación:** `/Parcial2`

El proyecto insignia del repositorio. Es una plataforma de e-commerce construida con una arquitectura de microservicios simulada y orquestada con Docker.

  * **Arquitectura:**
      * **Frontend:** React + TypeScript + Vite (Consumo de API).
      * **Backend:** Java Spring Boot 3 (Seguridad JWT, REST API).
      * **Base de Datos:** MongoDB (Desplegada en Atlas para prod / Contenedor para dev).
      * **DevOps:** Docker Compose para orquestar los 3 servicios.
  * **Conceptos Clave:** `Spring Data MongoDB`, `MongoRepository`, `Docker Networks`, `JWT Authentication`.

### 2\. 🐚 Scripting y Consultas Avanzadas (Parcial 1 & Quiz 1)

**Ubicación:** `/Parcial1` y `/Quiz1`

Ejercicios prácticos centrados en el dominio del **MongoDB Query Language (MQL)**.

  * **Parcial 1:** Scripts complejos para un sistema de inventario. Incluye uso de `$lookup`, `$unwind`, `$group` (Aggregation Framework) y actualizaciones atómicas.
  * **Quiz 1:** Modelado de datos para una Biblioteca. Demostración de **Modelado de Documentos** (Embedding vs Referencing) insertando libros prestados dentro del documento de usuario.

### 3\. 🟢 Integración con Node.js (ClaseMongo6)

**Ubicación:** `/ClaseMongo6`

Introducción a la conexión de aplicaciones mediante ODMs.

  * **Stack:** Node.js + Express.
  * **Tecnología:** `Mongoose` (ODM).
  * **Funcionalidad:** API CRUD básica para gestión de productos, demostrando la definición de Esquemas (`Schema`) y Modelos en JavaScript.

-----

## 🛠️ Stack Tecnológico

| Categoría | Tecnologías |
| :--- | :--- |
| **Base de Datos** | **MongoDB**, MongoDB Atlas, Compass |
| **Backend** | **Spring Boot** (Java 17), **Node.js** (Express) |
| **Frontend** | **React**, TypeScript, Tailwind CSS |
| **Infraestructura** | **Docker**, Docker Compose |
| **Herramientas** | Maven, Postman/Thunder Client |

-----

## 🚀 Guía Rápida de Ejecución

### Para el Proyecto Principal (FashionLine)

Este proyecto está totalmente contenerizado. Si tienes Docker instalado:

1.  Navega a la carpeta:
    ```bash
    cd Parcial2
    ```
2.  Levanta la infraestructura completa:
    ```bash
    docker-compose -p fashionline up -d
    ```
3.  Accede a los servicios:
      * **Frontend:** http://localhost:5173
      * **API Swagger:** http://localhost:8091/swagger-ui.html
      * **Mongo Express (BD):** localhost:27018

### Para los Scripts (Parcial 1 / Quiz 1)

Requieren tener instalado `mongosh` o MongoDB Compass.

1.  Abre el archivo `.js` o `.mongodb` en VS Code (con la extensión de MongoDB) o copia el contenido en tu terminal `mongosh`.
2.  Ejecuta las sentencias para crear las colecciones y realizar las consultas de agregación.

### Para el API de Node.js (ClaseMongo6)

```bash
cd ClaseMongo6
npm install
npm run dev
# Servidor corriendo en http://localhost:3001
```

-----

## 🧠 Conceptos de Base de Datos Aprendidos

1.  **Diferencias SQL vs NoSQL:** Transición de esquemas rígidos a esquemas flexibles (Schema-less).
2.  **Aggregation Pipeline:** Uso de etapas (`$match`, `$group`, `$project`) para análisis de datos en el servidor.
3.  **Modelado de Datos:** Decisiones de diseño sobre cuándo embeber documentos (1:Pocos) vs referenciar documentos (1:Muchos).
4.  **Persistencia Políglota:** Conexión a MongoDB desde entornos asíncronos (Node.js) y entornos tipados/síncronos (Java Spring).

-----

*Repositorio académico para la asignatura de Bases de Datos II.*