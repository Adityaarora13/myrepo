Case Study: Employee Management System (EMS) 
Objective: 
Build an Employee Management System using Spring Boot that allows CRUD operations on employee data, role-based access control, and integration with a MySQL database. 
 
Project Requirements: 
1. Tech Stack: 
Java 17+ 
Spring Boot 3.x 
Spring Data JPA 
Spring Security (JWT-based auth) 
MySQL 
Maven 
Postman (for API testing) 
Lombok (to reduce boilerplate) 
 
Use Case: 
Description: 
A mid-size company wants to build an internal EMS where: 
Admins can add, update, and delete employee records. 
Employees can view their own profiles. 
HR can view all employees but cannot delete or modify admin records. 
 
Functional Requirements: 
Login System with JWT authentication. 
Role-Based Access: Admin, HR, Employee. 
CRUD Operations: 
Add employee (Admin only) 
View all employees (Admin & HR) 
Update employee (Admin) 
View own profile (Employee)     
Store data in MySQL using Spring Data JPA. 
 
Key Entities: 
User: ID, username, password, role (ADMIN, HR, EMPLOYEE) 
Employee: ID, name, department, email, phone, reporting manager	 
 
APIs: 
POST /auth/login – Login with JWT response 
POST /employees/ – Create employee (Admin only) 
GET /employees/ – Get all employees (Admin, HR)
GET/employees/{joiningDate} - Only Admin can access
GET /employees/{id} – View specific employee 
PUT /employees/{id} – Update employee (Admin) 
DELETE /employees/{id} – Delete employee (Admin) 
 
Intermediate Concepts Covered: 
JWT token-based authentication with Spring Security 
Entity Relationships using JPA 
Exception handling using @ControllerAdvice 
DTOs and Model Mapping 
Environment-based config (application.yml) 
