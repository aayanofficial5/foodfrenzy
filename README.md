# FoodFrenzy
FoodFrenzy is a comprehensive system designed for managing customers, inventory, and orders. It offers secure authentication, role-based access control, and database integration using MySQL. Built with Spring Boot and Thymeleaf, the application provides a seamless experience for admin and staff members.


## Features

- **Customer Management**: Easily add, update, and delete customer information.
- **Inventory Management**: Keep track of your inventory items, including stock levels and pricing.
- **Order Management**: Manage customer orders, including order creation, updates, and status tracking.
- **User Authentication**: Secure login and authentication for admin and staff members.
- **Role-Based Access Control**: Define roles and permissions for different user types.
- **Thymeleaf Templates**: Utilizes Thymeleaf for dynamic HTML templates.
- **Database Integration**: Integrated with MySQL for data storage and retrieval.

## Technology Stack

- **Backend**: Spring Boot, Java 8, Spring MVC, Spring Data JPA (Hibernate)
- **Frontend**: Thymeleaf, HTML, CSS, JavaScript
- **Database**: MySQL
- **IDE**: Eclipse, Spring Tool Suite (STS)

## Prerequisites

Before running this project, ensure you have the following installed:

- Java 8
- MySQL
- Maven
- Eclipse or Spring Tool Suite (STS)

## Setup and Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/aayanofficial5/foodfrenzy.git
    ```

2. Navigate to the project directory:
    ```bash
    cd foodfrenzy
    ```

3. Configure MySQL Database:
    - Create a new MySQL database.
    - Update `application.properties` with your MySQL credentials:
      ```properties
      spring.datasource.name=FoodFrenzy
      spring.datasource.url=jdbc:mysql://localhost:3306/FoodFrenzy?createDatabaseIfNotExist=true
      spring.datasource.username=root
      spring.datasource.password=1234
      spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
      spring.jpa.hibernate.ddl-auto=update
      server.port=8081
      ```

4. Run the project:
    ```bash
    mvn spring-boot:run
    ```

5. Access the application:
    - Navigate to `http://localhost:8081` in your browser. 

## Project Structure

```bash
src/
├── main/
│   ├── java/
│   │   └── com.example.demo/
│   │       ├── config/            # Configuration classes (e.g., SecurityConfig)
│   │       ├── controllers/       # Contains all controller classes (Admin, User, Product, Order, Home)
│   │       ├── entities/          # Entity classes mapped to MySQL tables
│   │       ├── loginCredentials/  # Classes for handling admin and user login data
│   │       ├── repositories/      # Repository interfaces for database CRUD operations
│   │       ├── services/          # Service layer implementing business logic
│   │       ├── count/             # Utility and helper logic (e.g., Logic.java)
│   │       └── FoodFrenzyApplication.java  # Application entry point
│   │
│   ├── resources/
│   │   ├── static/                # Static assets such as CSS, images, and JavaScript
│   │   │   ├── css/               # Stylesheets for all pages
│   │   │   ├── Images/            # Image resources used in templates
│   │   │   └── JavaScript/        # Frontend scripts for interactivity
│   │   ├── templates/             # Thymeleaf templates (HTML pages for UI)
│   │   └── application.properties # Project configuration (DB, port, etc.)
│   │
│   └── webapp/                    # Optional web resources (not used in this project)
│
└── test/
    └── java/
        └── com.example.demo/      # Unit and integration test cases
