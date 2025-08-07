# CarShowroom1
🚗 Car Showroom Backend API
Welcome to the Car Showroom Backend API! This is a robust and scalable RESTful API built with Spring Boot and Java, backed by a PostgreSQL database. It provides all the necessary functionality to manage a car showroom's inventory.

✨ Features
Car Management: Create, read, update, and delete (CRUD) operations for cars.

RESTful Endpoints: A clean and intuitive API design following REST principles.

Data Persistence: Uses Spring Data JPA to interact with a PostgreSQL database.

Robustness: Built with Spring Boot's dependency injection and auto-configuration for a reliable application.

🚀 Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

Prerequisites
Java 17 or higher

Maven

PostgreSQL database

An IDE (like IntelliJ IDEA, Eclipse, or VS Code)

Setup
Clone the repository:

git clone https://github.com/your-username/car-showroom.git
cd car-showroom

Configure the Database:
First, ensure you have a PostgreSQL instance running. Then, connect to your database and execute the following SQL to create the car table:

CREATE TABLE car (
    id SERIAL PRIMARY KEY,
    make VARCHAR(255) NOT NULL,
    model VARCHAR(255) NOT NULL,
    year INTEGER NOT NULL,
    color VARCHAR(255),
    price DOUBLE PRECISION
);

Update Configuration:
Open the src/main/resources/application.properties file and update the database credentials with your own.

spring.datasource.url=jdbc:postgresql://localhost:5432/car_showroom
spring.datasource.username=your_username
spring.datasource.password=your_password

Run the Application:
You can run the application directly from your IDE or use Maven from the command line:

./mvnw spring-boot:run

The application will start on port 8080.

💻 API Endpoints
The API is fully documented and can be interacted with using tools like curl, Postman, or a web frontend.

Method

Endpoint

Description

Request Body (JSON)

POST

/api/cars

Creates a new car

{"make":"Ford","model":"Mustang","year":2021,"color":"Red","price":45000.00}

GET

/api/cars

Retrieves all cars

None

GET

/api/cars/{id}

Retrieves a car by ID

None

PUT

/api/cars/{id}

Updates a car by ID

{"make":"Ford","model":"Mustang","year":2022,"color":"Blue","price":47000.00}

DELETE

/api/cars/{id}

Deletes a car by ID

None

🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check the issues page for open tasks.

📄 License
Distributed under the MIT License. See LICENSE for more information.
