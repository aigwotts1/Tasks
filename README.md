# Tasks Tracker Assignment

JAVA BACKEND TASK TRACKER PROJECT : Built Spring Boot project consisting of entity i.e. Tasks having fields Id,Title,Descrition,Due Date.
Project can perform CRUD Operations to add,delete,update,view all Tasks and proper validations has been done for API endpoints, Database used is PostgreSQL, project hosted locally and endpoints documentation via Swagger. USED TECHNOLOGIES : Maven, SpringBoot, MongoDb, Swagger, Junit5 Mockito and Github.

------------------

How to Run - 

Prerequisites:

Make sure you have Java JDK installed on your machine. Spring Boot requires Java 8 or later versions.
Install Maven.

Clone the Project:
Clone or download the project.

Using Maven You can run the Spring Boot Project.

Dependencies I used : Spring Boot Starter Web, Spring Boot Starter JDBC,Spring Boot Starter Validation, Spring Boot Starter Test, PostgreSql , Open Api Documentation for Using APIs via Swagger.

5. Configure Spring Boot Application for PostgreSql:
   Application Properties:
     # PostgreSql connection properties
     spring.datasource.url=<url>
     spring.datasource.username=<username>
     spring.datasource.password=<password>

port i used : server.port = 9999
-------------------
Api Documentation for each route in JSON format:

1.Add Task
Adds a new task to the system.

Endpoint: POST /tasks
Request Body:
{
  "id": "1",
  "title":"title",
  "description":"description",
  "dueDate":"09/02/2002"
}
Response (Status 201 Created) :
{
  "id": "1",
  "title":"title",
  "description":"description",
  "dueDate":"09/02/2002"
}


2. Get All Tasks
Retrieves a list of all tasks in the system.

Endpoint: GET /tasks
Response (Status 200 OK):
[
  {
  "id": "1",
  "title":"title",
  "description":"description",
  "dueDate":"09/02/2002"
  },
  {
  "id": "2",
  "title":"title2",
  "description":"description2",
  "dueDate":"09/02/2002"
  },
  ...
]


3.Delete Task by ID
Deletes the tasks with the specified ID from the system.

Endpoint: DELETE /tasks/{id}
Path Variable:
{id}: The ID of the task to be deleted.
Response (Status 204 No Content):
This endpoint does not return any content in the response body.


4.Update Tasks by ID
Updates the task with the specified ID and the task in the system.
(you have to give id as well as details as task as requestBody to be modified)

Endpoint: PUT /tasks/{id}
Path Variable:
{id}: The ID of the task to be updated.

Path Variable: id,
Request Body:
 {
  "id": "1",
  "title":"title",
  "description":"description",
  "dueDate":"09/02/2002"
  }
Response (Status 200 OK):
 {
  "id": "1",
  "title":"title",
  "description":"description",
  "dueDate":"09/02/2002"
  }

5. Get Task By Id:
Get the task with the specified ID and the task in the system.

Endpoint: GET /tasks/{id}
Path Variable:
{id}: The ID of the task to be updated.

Path Variable: id,

Response (Status 200 OK):
 {
  "id": "1",
  "title":"title",
  "description":"description",
  "dueDate":"09/02/2002"
  }

-----------------------

Proper Validations and error handling and Junit5 Mockito testing has been done with coverage for service as well as Rest Controller layer.

-----------------------
Completed The Assignment with the learnings I had in past and by learning new concepts needed for this project via internet, hope it fulfills the requirements :)
