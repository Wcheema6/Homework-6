For Windows:

mvnw.cmd spring-boot:run
Wait until you see:
Started CampusTaskboardApplication
Open the API in your browser:
http://localhost:8080/api/tasks
H2 Database Console

You can view the database using H2:

http://localhost:8080/h2-console

Use:

JDBC URL: jdbc:h2:mem:taskboarddb
Username: sa
Password: (leave blank)

Run:

SELECT * FROM tasks;

to view stored data.

API Endpoints Documentation

Base URL:

http://localhost:8080/api/tasks
GET all tasks
GET /api/tasks

Returns all tasks.

GET task by ID
GET /api/tasks/{id}

Returns a specific task.

POST create task
POST /api/tasks

Body:

{
  "title": "My task",
  "description": "Testing database",
  "priority": "HIGH",
  "completed": false
}
PUT update task
PUT /api/tasks/{id}

Updates a task.

DELETE task
DELETE /api/tasks/{id}

Deletes a task.

New HW6 Endpoints
Completed tasks
GET /api/tasks/completed

Returns all completed tasks.

Incomplete tasks
GET /api/tasks/incomplete

Returns all incomplete tasks.

Filter by priority
GET /api/tasks/priority/HIGH

Returns tasks with a specific priority.

Search tasks
GET /api/tasks/search?keyword=task

Searches tasks by title or description.

Pagination
GET /api/tasks/paginated?page=0&size=5

Returns paginated results.

Notes
This project uses Spring Boot, Spring Data JPA, H2 Database, and Validation.
Tasks are now stored in a database instead of memory.
Data is reset when the application stops because H2 is an in-memory database.
