# Basic REST API with Spring Boot, PostgreSQL, and JDBC

## Project Overview

This project is a basic REST API built using Java Spring Boot. It leverages the PostgreSQL database and JDBC for data persistence and interaction.

---

## Features

- **RESTful Endpoints**: Perform CRUD operations on the database.
- **PostgreSQL Database**: Uses PostgreSQL for reliable and scalable database operations.
- **JDBC Integration**: Interacts with the PostgreSQL database using JDBC.

---

## Technologies Used

- **Java**
- **Spring Boot**
    - Spring Web
    - Spring JDBC
- **PostgreSQL Database**
- **Maven**

---

## Setup Instructions

### Prerequisites

1. **Java Development Kit (JDK)**: Ensure JDK 17 or later is installed.
2. **Maven**: Install Maven for dependency management.
3. **PostgreSQL**: Ensure PostgreSQL is installed and running.

### Steps to Run the Project

1. **Clone the Repository**:

   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. **Set Up PostgreSQL Database**:

    - Create a database named `runnerz_db` (or modify `application.properties` for your database name).
    - Ensure the username and password match the configuration in `application.properties`.

3. **Build the Project**:

   ```bash
    go to --> https://start.spring.io
   ```

4. **Run the Application**:

   ```bash
   by looking the dependencies in the pom.xml file, you can run the application
   ```

### Configuration

All configurations are located in the `application.properties` file. Default settings include:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/runnerz_db
spring.datasource.driverClassName=org.postgresql.Driver
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

---

## API Endpoints

| HTTP Method | Endpoint         | Description              |
| ----------- |------------------| ------------------------ |
| GET         | `/api/runs`      | Fetch all runs           |
| GET         | `/api/runs/{id}` | Fetch a run by ID        |
| POST        | `/api/runs`      | Create a new run         |
| PUT         | `/api/runs/{id}` | Update an existing run   |
| DELETE      | `/api/runs/{id}` | Delete a run             |

---

## Project Structure

```
src
├── main
│   ├── java
│   │   └── com.example.runnerz
│   │       └── run
│   │           ├── Location
│   │           ├── Run
│   │           ├── RunController
│   │           ├── RunJsonDataLoader
│   │           ├── RunNotFoundException
│   │           ├── RunRepository
│   │           └── Runs
│   └── resources
│       ├── application.properties
│       ├── schema.sql
│       └── data
│           └── runs.json
```

- **RunController**: Handles incoming HTTP requests for the `Run` entity.
- **RunRepository**: Manages database operations related to `Run` using JDBC.
- **RunJsonDataLoader**: Handles JSON data loading operations.
- **RunNotFoundException**: Custom exception for handling run-related errors.
- **schema.sql**: Contains the database schema definition.
- **data**: Directory for additional data resources.

---

## Testing the API

- Use tools like **Postman** or **cURL** to test the endpoints.
- Example cURL command to fetch all runs:
  ```bash
  curl -X GET http://localhost:8080/api/runs
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

