# Homework-6
Homework 6 for CISC.
# Campus Task Board API – HW6

## Project Description

In this project, I extended my Homework 5 API by adding a database using Spring Data JPA and H2. 

In HW5, tasks were stored in an ArrayList, which meant all data was lost when the application restarted. In HW6, I replaced that with a real database so tasks are now stored persistently while the application is running.

Each task includes:
- id
- title
- description
- completed status
- priority (LOW, MEDIUM, HIGH)
- timestamps (createdAt, updatedAt)

I also added new features such as filtering, searching, and pagination.

---

## How to Run the Application

1. Open the project folder in VS Code or IntelliJ.

2. Make sure Java 17 or newer is installed.

3. Open a terminal inside the project folder.

4. Run the application:

```bash
./mvnw spring-boot:run
