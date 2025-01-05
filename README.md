# University Registration System

This project is a University Registration System built with Java, Maven, and Oracle Database. It allows students to register for courses, view their schedules, and interact with university-related features. The system also provides administrative features to manage students, courses, and registrations.

## Project Structure

```
.
├── .mvn/                        # Maven wrapper files
├── .settings/                   # IDE settings (Eclipse or IntelliJ)
├── src/                         # Source code for the project
│   └── main/
│   └── test/
├── target/                      # Compiled files (JARs, classes, etc.)
├── mvnw                         # Maven wrapper script for Unix-like OS
├── mvnw.cmd                     # Maven wrapper script for Windows
├── pom.xml                      # Maven Project Object Model (POM) file
├── HELP.md                      # Help documentation
└── README.md                    # Project documentation
```

## Features

- **Student Registration**: Allows students to register for courses online.
- **Course Management**: Admins can add, remove, and manage courses.
- **Student Dashboard**: Students can view registered courses, grades, and other relevant information.
- **Admin Dashboard**: Admins can manage student data, course schedules, and more.

## Technology Stack

### Backend:
- **Programming Language**: Java
- **Framework**: Spring Boot (or other Java frameworks)
- **Database**: Oracle
- **Build Tool**: Maven
- **Packaging**: JAR (Java Archive)

### Frontend:
- **Framework**: React/Angular (or your choice of frontend framework)
- **Styling**: CSS, Bootstrap/Tailwind

## Prerequisites

- **Java 11+** (or compatible version)
- **Maven** (for building and managing the project)
- **Oracle Database** (for storing data)
- **Kafka** (if used for streaming data)

## Setup

### Backend Setup

1. Clone the repository:

    ```bash
    git clone https://github.com/cmaldikar/University_Registration_System.git
    ```

2. Navigate to the project directory:

    ```bash
    cd University_Registration_System
    ```

3. Build the project using Maven:

    ```bash
    mvn clean install
    ```

4. Set up your **Oracle Database** and configure the connection in the `application.properties` (or similar) file. Example configuration:

    ```properties
    spring.datasource.url=jdbc:oracle:thin:@your-db-url:1521:xe
    spring.datasource.username=your-username
    spring.datasource.password=your-password
    spring.datasource.driver-class-name=oracle.jdbc.OracleDriver
    ```

5. Run the backend server:

    ```bash
    mvn spring-boot:run
    ```

### Frontend Setup

1. Navigate to the frontend directory:

    ```bash
    cd University_Registration_System/FrontEnd
    ```

2. Install the frontend dependencies:

    ```bash
    npm install
    ```

3. Start the frontend server:

    ```bash
    npm start
    ```

## Database Schema

The system uses **Oracle Database** to store student information, course details, and registration records. Below is an example of the key tables:

- **Students**
  - student_id (PK)
  - first_name
  - last_name
  - email
  - registration_date
  - etc.

- **Courses**
  - course_id (PK)
  - course_name
  - course_code
  - instructor_id
  - etc.

- **Registrations**
  - registration_id (PK)
  - student_id (FK)
  - course_id (FK)
  - registration_date
  - etc.

## Running Tests

1. Ensure the backend is running.
2. Use your testing framework (e.g., JUnit for Java) to run the backend tests.
3. For the frontend, run:

    ```bash
    npm test
    ```

## Contributing

Contributions are welcome! If you would like to contribute to this project, please fork the repository, create a feature branch, and submit a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
