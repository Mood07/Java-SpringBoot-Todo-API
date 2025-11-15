# 📝 Java Spring Boot Todo API

A production-ready **Spring Boot REST API** built with **Java**, **MySQL**, **JPA/Hibernate**, and a clean **layered architecture**.  
Implements full CRUD operations for Todo items with DTO mapping, validation, service layer abstraction, and global exception handling.

Perfect for showcasing **Java Backend Development** skills in your GitHub portfolio or CV.

---

## 🚀 Features

- Create, read, update, delete Todo items  
- DTO mapping for clean API responses  
- MySQL database integration  
- JPA + Hibernate ORM  
- Layered architecture (Controller → Service → Repository)  
- Exception handling  
- Request validation  
- High-quality REST API design  

---

## 🧱 Project Structure

```
src/main/java/com/mood/todoapi/
│
├── controller/
│     └── TodoController.java
│
├── service/
│     ├── TodoService.java
│     └── impl/
│           └── TodoServiceImpl.java
│
├── repository/
│     └── TodoRepository.java
│
├── entity/
│     └── Todo.java
│
├── dto/
│     └── TodoDTO.java
│
├── exception/
│     ├── ResourceNotFoundException.java
│     └── GlobalExceptionHandler.java (optional)
│
└── TodoApiApplication.java
```

---

## 🗄 MySQL Configuration

### 1️⃣ `application.properties` (GitHub-safe version)

```
spring.datasource.url=jdbc:mysql://localhost:3306/todo_db?createDatabaseIfNotExist=true&useSSL=false&serverTimezone=UTC
spring.datasource.username=YOUR_DB_USERNAME
spring.datasource.password=YOUR_DB_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQLDialect

spring.profiles.active=local
```

⚠️ Your real DB credentials must **NOT** be pushed to GitHub.

---

### 2️⃣ `application-local.properties` (local only)

```
spring.datasource.username=root
spring.datasource.password=YOUR_REAL_PASSWORD
```

Add this to `.gitignore`:

```
src/main/resources/application-local.properties
```

---

## ▶ How to Run

### Build:
```
./gradlew build
```

### Run:
```
./gradlew bootRun
```

Or via IntelliJ → Right-click `TodoApiApplication` → Run

---

## 📡 API Endpoints

### ➕ Create Todo  
`POST /api/todos`
```json
{
  "title": "Learn Spring Boot",
  "description": "Build a full REST API",
  "completed": false
}
```

### 📋 Get All  
`GET /api/todos`

### 🔍 Get by ID  
`GET /api/todos/{id}`

### ✏️ Update Todo  
`PUT /api/todos/{id}`
```json
{
  "title": "Updated Title",
  "description": "Updated Desc",
  "completed": true
}
```

### ❌ Delete  
`DELETE /api/todos/{id}`

---

## 🧰 Technologies Used

| Category | Technology |
|----------|------------|
| Language | Java 21 / 23 |
| Framework | Spring Boot 3 |
| REST Layer | Spring Web |
| ORM | JPA + Hibernate |
| Database | MySQL |
| Build Tool | Gradle |
| JSON | Jackson |
| IDE | IntelliJ IDEA |

---

## 👨‍💻 Author

**Berke Arda Türk**  
Data Science & AI Enthusiast | Computer Science (B.ASc)  
[🌐 Portfolio Website](https://berke-turk.web.app/) • [💼 LinkedIn](https://www.linkedin.com/in/berke-arda-turk/) • [🐙 GitHub](https://github.com/Mood07)

