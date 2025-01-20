# Basic REST API with Spring Boot, H2 Database, and JDBC

## Project Overview

This project is a basic REST API built using Java Spring Boot. It leverages the H2 in-memory database and JDBC for data persistence and interaction.

---

## Features

- **RESTful Endpoints**: Perform CRUD operations on the database.
- **In-memory Database**: Uses H2 for lightweight and fast database operations.
- **JDBC Integration**: Interacts with the H2 database using JDBC.

---

## Technologies Used

- **Java**
- **Spring Boot**
    - Spring Web
    - Spring JDBC
- **H2 Database**
- **Maven**

---

## Setup Instructions

### Prerequisites

1. **Java Development Kit (JDK)**: Ensure JDK 17 or later is installed.
2. **Maven**: Install Maven for dependency management.

### Steps to Run the Project

1. **Clone the Repository**:

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Build the Project**:

   ```bash
   mvn clean install
   ```

3. **Run the Application**:

   ```bash
   mvn spring-boot:run
   ```

4. **Access the H2 Database Console**:

    - Open a browser and navigate to `http://localhost:8080/h2-console`.
    - Use the following credentials to connect:
        - **JDBC URL**: `jdbc:h2:mem:testdb`
        - **Username**: `sa`
        - **Password**: *(leave blank)*

### Configuration

All configurations are located in the `application.properties` file. Default settings include:

```properties
spring.h2.console.enabled=true
spring.h2.console.path=/h2-console
spring.datasource.url=jdbc:h2:mem:testdb
spring.datasource.driverClassName=org.h2.Driver
spring.datasource.username=sa
spring.datasource.password=
spring.datasource.platform=h2
```

---

## API Endpoints

| HTTP Method | Endpoint      | Description             |
| ----------- | ------------- | ----------------------- |
| GET         | `/items`      | Fetch all items         |
| GET         | `/items/{id}` | Fetch item by ID        |
| POST        | `/items`      | Create a new item       |
| PUT         | `/items/{id}` | Update an existing item |
| DELETE      | `/items/{id}` | Delete an item          |

---

## Project Structure

```
src
├── main
│   ├── java
│   │   └── com.example.restapi
│   │       ├── controller
│   │       ├── service
│   │       ├── model
│   │       └── repository
│   └── resources
│       ├── application.properties
│       └── data.sql
```

- **Controller**: Handles incoming HTTP requests.
- **Service**: Contains business logic.
- **Repository**: Manages database operations using JDBC.
- **Data.sql**: Preloads the database with sample data on startup.

---

## Testing the API

- Use tools like **Postman** or **cURL** to test the endpoints.
- Example cURL command to fetch all items:
  ```bash
  curl -X GET http://localhost:8080/items
  ```

---

## Future Enhancements

- Add pagination and sorting.
- Implement validation for request payloads.
- Integrate with a frontend client.
- Add unit and integration tests.

---

## License

This project is licensed under the MIT License. See `LICENSE` for details.

---

## Author

[Your Name]

For any questions or issues, please contact: [Your Email Address]

