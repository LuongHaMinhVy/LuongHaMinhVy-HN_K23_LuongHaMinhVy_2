# 🛒 Sales Management System (newProjectSales)

Backend e-commerce project built with **Spring Boot**.  
This project provides RESTful APIs for authentication, product management, order processing, and role-based access control.

---

## 🚀 Tech Stack

- Java 21
- Spring Boot
- Spring Security
- JWT Authentication
- Spring Data JPA
- MySQL
- Gradle
- Cloudinary (Media storage)
- Spring Mail (Email service)

---

## 📌 Main Features

### 🔐 Authentication & Authorization
- User Registration
- User Login (JWT-based authentication)
- Password encryption using BCrypt
- Role-based access control (ADMIN, CUSTOMER, etc.)
- Email verification (if configured)

### 📦 Product Management
- Create / Update / Delete Products
- Product listing with pagination
- Product filtering & search
- Soft delete handling

### 🛍️ Cart & Orders
- Add to cart
- Update cart items
- Place order
- Order status management
- Stock handling

### 📊 Additional
- Pagination wrapper response
- Standardized API response structure
- Secure RESTful design
- Exception handling

---

## 🏗️ Project Structure

```
src/
 ├── main/
 │    ├── java/
 │    │     ├── config/          # Security configuration
 │    │     ├── controller/      # REST controllers
 │    │     ├── service/         # Business logic
 │    │     ├── repository/      # JPA repositories
 │    │     ├── dto/             # Data transfer objects
 │    │     ├── entity/          # JPA entities
 │    │     └── util/            # Utility classes (JWT, etc.)
 │    └── resources/
 │          ├── application.yml
 │          └── ...
 └── test/
```

---

## ⚙️ Setup & Installation

### 1️⃣ Clone Repository

```bash
git clone https://github.com/LuongHaMinhVy/newProjectSales.git
cd newProjectSales
```

---

### 2️⃣ Configure Database

Update `application.yml`:

```yaml
spring:
  datasource:
    url: jdbc:mysql://localhost:3306/your_database
    username: your_username
    password: your_password

  jpa:
    hibernate:
      ddl-auto: update
    show-sql: true
```

---

### 3️⃣ Configure JWT

```yaml
jwt:
  secret: your_secret_key
  expiration: 86400000
```

---

### 4️⃣ (Optional) Configure Mail

```yaml
spring:
  mail:
    host: smtp.gmail.com
    port: 587
    username: your_email
    password: your_app_password
```

---

### 5️⃣ Run Project

Using Gradle:

```bash
./gradlew bootRun
```

Or build JAR:

```bash
./gradlew build
java -jar build/libs/*.jar
```

---

## 📡 Sample API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register new user |
| POST | `/api/auth/login` | Login & get JWT |
| GET | `/api/products` | Get product list |
| POST | `/api/products` | Create product (Admin) |
| PUT | `/api/products/{id}` | Update product |
| DELETE | `/api/products/{id}` | Soft delete product |
| POST | `/api/orders` | Create order |

---

## 🧪 Running Tests

```bash
./gradlew test
```

---

## 📖 API Response Format

All APIs return standardized structure:

```json
{
  "data": {},
  "message": "Success",
  "success": true,
  "errors": null,
  "timeStamp": "2026-03-02T10:00:00"
}
```

---

## 🔒 Security

- JWT-based stateless authentication
- Password hashing with BCrypt
- Role-based authorization
- Secure API endpoint configuration

---

## 📄 License

This project is for learning and development purposes.

---

## 👤 Author

**Luong Ha Minh Vy**  
Backend Developer (Spring Boot)
