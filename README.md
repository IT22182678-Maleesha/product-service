# product-service

A RESTful microservice for managing products built with Spring Boot.

## Overview

This Product Service provides a simple API to perform CRUD operations on products. It uses an H2 in-memory database for data persistence and includes Swagger UI for API documentation and testing.

## Technologies Used

- **Java 21**
- **Spring Boot 4.1.0-SNAPSHOT**
- **Spring Web** - REST API implementation
- **Spring Data JPA** - Database operations
- **H2 Database** - In-memory database
- **Swagger/OpenAPI** - API documentation
- **Maven** - Build tool

## Prerequisites

- JDK 21 or later
- Maven 3.6+
- Your favorite IDE (IntelliJ, Eclipse, VS Code)

## Getting Started

### Clone the repository

git clone https://github.com/IT22182678-Maleesha/product-service.git


## Build the project
./mvnw clean install

## Run the application
./mvnw spring-boot:run

## API Documentation
Once the application is running, you can access:

Swagger UI: http://localhost:8080/swagger-ui.html

OpenAPI JSON: http://localhost:8080/v3/api-docs

H2 Console: http://localhost:8080/h2-console

## API Endpoints
Method	URL	Description
POST	/products	Create a new product
GET	/products	Get all products
GET	/products/{id}	Get a product by ID
DELETE	/products/{id}	Delete a product by ID

## Create a Product

POST /products
{
  "name": "Laptop",
  "price": 999.99
}

Response (201 Created)
{
  "id": 1,
  "name": "Laptop",
  "price": 999.99
}

## Get All Products

GET /products

Response (200 OK)
[

  {
    "id": 1,
    "name": "Laptop",
    "price": 999.99
  },
  {
    "id": 2,
    "name": "Mouse",
    "price": 29.99
  }
  
]

## Get Product by ID
GET /products/1

Response (200 OK)
{
  "id": 1,
  "name": "Laptop",
  "price": 999.99
}

## Delete Product
DELETE /products/1

Response

204 No Content (if successful)

404 Not Found (if product doesn't exist)

## Database Configuration
The application uses H2 in-memory database with the following configuration:

spring.datasource.url=jdbc:h2:mem:productdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true

spring.h2.console.enabled=true
spring.h2.console.path=/h2-console

Features
✅ RESTful API design

✅ CRUD operations for products

✅ In-memory H2 database

✅ Swagger/OpenAPI documentation

✅ JPA for data persistence

✅ Maven build tool

✅ Spring Boot auto-configuration


