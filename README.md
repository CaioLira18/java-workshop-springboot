# Spring Boot Web Services with JPA/Hibernate

This project demonstrates a comprehensive implementation of RESTful web services using Spring Boot with JPA/Hibernate for data persistence.

## Project Objectives

- Create a Spring Boot Java application
- Implement domain models
- Structure logical layers: resource, service, repository
- Configure test database (H2)
- Populate the database
- Implement CRUD operations (Create, Retrieve, Update, Delete)
- Handle exceptions properly

## Technologies

- Java 17
- Spring Boot
- JPA / Hibernate
- H2 Database (test profile)
- PostgreSQL (dev profile)
- Maven

## Domain Model

The project implements a simple e-commerce domain model with the following entities:
- User
- Order
- Product
- Category
- OrderItem
- Payment

## Project Structure

The application follows a layered architecture:

1. **Resource Layer**: REST controllers that handle HTTP requests
2. **Service Layer**: Business logic implementation
3. **Repository Layer**: Data access using Spring Data JPA

## Features

- Complete CRUD operations for User entity
- Order processing with order items
- Many-to-many relationships between entities
- Product categorization
- Order status management
- Payment processing
- Exception handling with custom error responses

## Database Configuration

### Test Profile (H2)

The application comes with a preconfigured H2 in-memory database for testing purposes. The H2 console is enabled and accessible at `/h2-console`.

### Dev Profile (PostgreSQL)

For development, the application can be configured to use PostgreSQL.

## Getting Started

### Prerequisites

- Java 17
- Maven

### Installation

1. Clone the repository
```
git clone https://github.com/yourusername/workshop-springboot-jpa.git
```

2. Navigate to the project directory
```
cd workshop-springboot-jpa
```

3. Build the project
```
mvn clean install
```

4. Run the application
```
mvn spring-boot:run
```

## API Endpoints

### Users

- `GET /users` - Retrieve all users
- `GET /users/{id}` - Retrieve a specific user
- `POST /users` - Create a new user
- `PUT /users/{id}` - Update a user
- `DELETE /users/{id}` - Delete a user

### Orders

- `GET /orders` - Retrieve all orders
- `GET /orders/{id}` - Retrieve a specific order

### Products

- `GET /products` - Retrieve all products
- `GET /products/{id}` - Retrieve a specific product

### Categories

- `GET /categories` - Retrieve all categories
- `GET /categories/{id}` - Retrieve a specific category

## Exception Handling

The application implements comprehensive exception handling with custom error responses:

- `ResourceNotFoundException` - When a requested resource is not found
- `DatabaseException` - When a database operation fails
- Custom error response format for better client-side error handling

## Sample JSON

### Create User
```json
{
  "name": "Bob Brown",
  "email": "bob@gmail.com",
  "phone": "977557755",
  "password": "123456"
}
```

### Update User
```json
{
  "name": "Bob Brown",
  "email": "bob@gmail.com",
  "phone": "977557755"
}
```

## License

This project is open source and available under the [MIT License](LICENSE).

## Acknowledgements

Based on the Spring Boot course by Dr. Nelio Alves at devsuperior.com.br
