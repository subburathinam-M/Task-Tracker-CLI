# 📝 Task Tracker CLI

## 🚀 Project Overview
Task Tracker CLI is a **Command Line Interface (CLI)** and **REST API**-based application built with **Spring Boot** and **MongoDB**. It helps users efficiently manage tasks, allowing them to **add, update, delete, and track tasks** directly from the CLI or through REST APIs.

## 🎯 Features
- 🏗️ **Create, Update, Delete Tasks**
- 🔄 **Change Task Status** (Todo, In-Progress, Done)
- 📋 **List Tasks** with filtering options
- 📡 **REST API & CLI support** for flexible usage
- 📜 **Swagger UI** for API Documentation
- 🌿 **MongoDB for Storage**  


## 🏗️ Tech Stack
🟢 **☕ Java 17** - Java                                          
🟢 **🌱 Spring Boot** - Backend Framework  
🟢 **📦 MongoDB** - NoSQL Database  
🟢 **🖥️ Spring Shell (CLI Support)** - CLI Interface  
🟢 **✨ Lombok** - Reducing Boilerplate Code  
🟢 **📜 Swagger (API Documentation)** - API Documentation  
🟢 **🛠️ Maven (Build & Dependency Management)** - Dependency Management  

## 📂 Project Structure
```
📦 tasktrackercli
 ┣ 📂 src/main/java/com/tasktracker/tasktrackercli
 ┃ ┣ 📂 entity        # Task Entity
 ┃ ┣ 📂 repository    # Database Repository
 ┃ ┣ 📂 service       # Business Logic Layer
 ┃ ┣ 📂 service/impl  # Service Implementations
 ┃ ┣ 📂 controller    # REST API Controllers
 ┃ ┣ 📂 cli           # CLI Commands
 ┣ 📂 resources
 ┃ ┣ 📜 application.properties  # Application Configuration
 ┣ 📜 pom.xml        # Maven Dependencies
 ┗ 📜 README.md      # Project Documentation
```

## 🛠️ Dependencies
```xml
<dependencies>
    <!-- Spring Boot & MongoDB -->
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-data-mongodb</artifactId>
    </dependency>
    <dependency>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-web</artifactId>
    </dependency>
    
    <!-- CLI Support -->
    <dependency>
        <groupId>org.springframework.shell</groupId>
        <artifactId>spring-shell-starter</artifactId>
    </dependency>
    
    <!-- Swagger for API Docs -->
    <dependency>
        <groupId>org.springdoc</groupId>
        <artifactId>springdoc-openapi-starter-webmvc-ui</artifactId>
        <version>2.3.0</version>
    </dependency>
</dependencies>
```

## 🚀 How to Run the Project
There are **two ways** to run this project:
### 1️⃣ Running via CLI (Command Line Interface)
```sh
# Navigate to the project directory
cd tasktrackercli

# Run the Spring Boot application
mvn spring-boot:run
```
#### **Step 1: Available CLI Commands:**
```sh
add "Task description"       # Add a new task
update <task_id> "New desc"  # Update task description
delete <task_id>            # Delete a task
status <task_id> done       # Change task status
list                        # List all tasks
```

#### **Step 2: Use CLI Commands**
```bash
# Add a new task
add --description "Finish project report"

# Update a task
update --id 123456 --description "Update project report"

# Delete a task
delete --id 123456

# Change task status
status --id 123456 --status "done"

# List all tasks
list
```

### 2️⃣ Running via Swagger (API UI)
After starting the application, open **Swagger UI** in your browser:
```
http://localhost:8080/tasktracker/api/swagger-ui.html
```
**Available API Endpoints:**
| Method  | Endpoint               | Description            |
|---------|------------------------|------------------------|
| `POST`  | `/api/tasks/add`       | Add a new task        |
| `PUT`   | `/api/tasks/update/{id}` | Update task description |
| `DELETE`| `/api/tasks/delete/{id}` | Delete a task         |
| `PATCH` | `/api/tasks/status/{id}` | Update task status    |
| `GET`   | `/api/tasks/list`      | Get tasks by status   |

## 📧 Contact
👤 **Subburathinam M**  
📩 Email: [subburathinam720@gmail.com](mailto:subburathinam720@gmail.com)  
📞 Phone: +91 XXXXX XXXXX  

🌟 **If you like this project, don't forget to give it a ⭐ on GitHub!**

