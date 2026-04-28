# 📌 Proyecto Microservicios - Plataforma FrikiTienda
El documento puede ser modificado a medida que el proyecto avanza.

## 📖 Descripción del Proyecto

El presente proyecto consiste en el desarrollo de una plataforma de ventas de productos gamer y cultura friki, implementada bajo una arquitectura de microservicios utilizando Spring Boot.

El sistema permite gestionar usuarios, productos, pedidos, pagos y otras funcionalidades, mediante servicios independientes que se comunican entre sí a través de APIs REST.

---

## 🎯 Objetivo

Diseñar e implementar una arquitectura distribuida basada en microservicios que permita:

* Separación de responsabilidades
* Comunicación entre servicios
* Persistencia independiente
* Implementación de reglas de negocio
* Manejo de errores y validaciones

---

## 🧱 Microservicios Implementados

| Microservicio         | Descripción           | Estado  |
| --------------------- | --------------------- | ------  |
| MS1 - Usuarios        | Gestión de usuarios   | ⬜      |
| MS2 - Microservicio   | Descripcion     ms2   | ⬜      |
| MS3 - Microservicio   | Descripcion     ms3   | ⬜      |
| MS4 - Microservicio   | Descripcion     ms4   | ⬜      |
| MS5 - Microservicio   | Descripcion     ms5   | ⬜      |
| MS6 - Microservicio   | Descripcion     ms6   | ⬜      |
| MS7 - Microservicio   | Descripcion     ms7   | ⬜      |
| MS8 - Microservicio   | Descripcion     ms8   | ⬜      |
| MS9 - Microservicio   | Descripcion     ms9   | ⬜      |
| MS10 -Microservicio   | Descripcion     ms10  | ⬜      |

---

## 🗄️ Persistencia de Datos 

* Cada microservicio posee su propia base de datos.
* No se comparten tablas entre servicios.
* Se mantiene la integridad referencial dentro de cada servicio.
* Se utiliza **MySQL o PostgreSQL** como motor de base de datos.

---

## 🧩 Estructura de Microservicios (Patrón CSR)

Cada microservicio implementa el patrón:

* **Controller** → Manejo de endpoints REST
* **Service** → Lógica de negocio
* **Repository** → Acceso a datos (JpaRepository)
* **Model (Entity)** → Representación de datos

---

## 🔄 Operaciones CRUD

Cada microservicio implementa operaciones CRUD completas sobre sus entidades principales:

Ejemplo:

### MS1 - Usuarios

* POST /usuarios → Crear usuario
* GET /usuarios → Obtener usuarios
* PUT /usuarios/{id} → Actualizar usuario
* DELETE /usuarios/{id} → Eliminar usuario

### MS3 - Catálogo

* GET /productos
* GET /productos/{id}
* GET /productos?categoria=

---

## ⚙️ Reglas de Negocio

El sistema implementa reglas de negocio relevantes, tales como:

* Validación de existencia de usuario antes de crear pedido
* Verificación de stock antes de confirmar compra
* Bloqueo de compra si el stock es insuficiente
* Cálculo de total de pedido

---

## ✅ Validaciones

Se implementan validaciones utilizando **Bean Validation (JSR 380)**:

* Campos obligatorios (@NotNull, @NotBlank)
* Validación de formato (correo, longitud, etc.)
* Validación de datos en los controladores mediante DTOs

---

## ⚠️ Manejo de Excepciones

* Uso de `@ControllerAdvice` para manejo global
* Respuestas con `ResponseEntity`
* Códigos HTTP adecuados:

  * 200 OK
  * 201 CREATED
  * 400 BAD REQUEST
  * 404 NOT FOUND

---
## 📡 Comunicación entre Microservicios

Los microservicios se comunican mediante:

* **REST APIs**
* Uso de **WebClient o Feign Client**

Ejemplo de flujo (Solo ejemplo):

1. Pedido consulta inventario
2. Inventario valida stock
3. Pedido solicita pago
4. Pago responde estado

---

## 📑 Endpoints REST

* Uso de rutas semánticas
* Métodos HTTP correctos (GET, POST, PUT, DELETE)
* Respuestas en formato JSON
* Uso de parámetros y request body estructurados

---

## 🧪 Pruebas

Se realizan pruebas de endpoints mediante:

* Postman

---

## 🛠️ Tecnologías Utilizadas

* Java 21+
* Spring Boot
* Spring Data JPA
* MySQL o PostgreSQL
* 
* 
* Maven

---

## 📂 Repositorio

El proyecto se gestiona mediante GitHub, cumpliendo con:

* Commits progresivos y descriptivos
* Trabajo colaborativo
* Organización del código por microservicio
* Un microservicio por proyecto,un proyecto por repositorio.

---

## 👥 Integrantes

* Nombre 1 
* Nombre 2
* Nombre 3

---

## 🚀 Estado del Proyecto

En desarrollo – implementación de microservicios base para evaluación parcial 2.

---

## 📌 Notas

Este README sirve como guía para el desarrollo del proyecto y será actualizado a medida que se implementen los microservicios.

---
