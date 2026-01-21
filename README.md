# PicPay Backend Service

A Spring Boot backend application for PicPay payment system implementation.

## 🚀 Technologies

- **Java 21**
- **Spring Boot 4.0.1**
- **Spring Cloud 2025.1.0**
- **Spring Data JPA**
- **Spring Web MVC**
- **Spring Validation**
- **OpenFeign** (for external API integration)
- **MySQL** (Database)
- **Maven** (Build tool)
- **Docker** (Containerization)

## 📋 Prerequisites

- Java 21 or higher
- Maven 3.6+
- Docker and Docker Compose
- Git

## 🛠️ Project Setup

### 1. Clone the Repository
```bash
git clone <repository-url>
cd picpay
```

### 2. Database Setup with Docker
Start the MySQL database using Docker Compose:

```bash
cd docker
docker-compose up -d
```

This will create:
- MySQL container on port `3306`
- Database: `picpay`
- User: `admin` / Password: `123`
- Root password: `123`
- Persistent volume for data storage

### 3. Application Configuration
The application uses the following default configuration:
- Application name: `picpay`
- Database connection will be configured to connect to the Docker MySQL instance

### 4. Build and Run

#### Using Maven Wrapper (Recommended)
```bash
# Build the project
./mvnw clean compile

# Run tests
./mvnw test

# Run the application
./mvnw spring-boot:run
```

#### Using Maven (if installed globally)
```bash
# Build the project
mvn clean compile

# Run tests
mvn test

# Run the application
mvn spring-boot:run
```

## 🏗️ Project Structure

```
picpay/
├── docker/
│   └── docker-compose.yml          # Database container configuration
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── hector/avlr/picpay/
│   │   │       └── PicpayApplication.java    # Main application class
│   │   └── resources/
│   │       ├── application.properties        # Application configuration
│   │       ├── static/                      # Static resources
│   │       └── templates/                   # Template files
│   └── test/
│       └── java/
│           └── hector/avlr/picpay/
│               └── PicpayApplicationTests.java
├── pom.xml                         # Maven dependencies and configuration
└── README.md                       # Project documentation
```

## 🔧 Key Dependencies

- **spring-boot-starter-data-jpa**: Database integration with JPA/Hibernate
- **spring-boot-starter-webmvc**: REST API development
- **spring-boot-starter-validation**: Input validation
- **spring-cloud-starter-openfeign**: HTTP client for external services
- **mysql-connector-j**: MySQL database driver

## 🐳 Docker Services

### MySQL Database
- **Image**: mysql:latest
- **Port**: 3306
- **Database**: picpay
- **Username**: admin
- **Password**: 123
- **Root Password**: 123

## 🚦 Getting Started

1. **Start the database**:
   ```bash
   cd docker && docker-compose up -d
   ```

2. **Verify database is running**:
   ```bash
   docker-compose ps
   ```

3. **Run the application**:
   ```bash
   ./mvnw spring-boot:run
   ```

4. **Access the application**:
   - The application will start on `http://localhost:8080`
   - Database will be available on `localhost:3306`

## 📝 Development Notes

- The project uses Spring Boot 4.0.1 with Java 21
- Database persistence is handled through Docker volumes
- The application is configured for development environment
- OpenFeign is included for external API integrations

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Run tests to ensure everything works
5. Submit a pull request

## 📄 License

This project is part of a PicPay backend implementation study.