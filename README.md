# CRM-System - Customer Relationship Management System

CRM-System is a full-stack web application designed to help businesses manage customer relationships efficiently. It features customer data management, sales tracking, and reporting capabilities. Built with **React** for the frontend and **Spring Boot** for the backend, CRM-System allows users to manage customer interactions, monitor sales performance, and generate reports, all within a secure environment.

This repository contains the source code for both the **front-end** (React) and **back-end** (Spring Boot) of the CRM-System.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Tech Stack](#tech-stack)
- [Key Features](#key-features)
- [Frontend & Backend Repositories](#frontend--backend-repositories)
- [Installation](#installation)
  - [Front-end Installation](#front-end-installation)
  - [Back-end Installation](#back-end-installation)
- [Running the Application](#running-the-application)
  - [Running the Front-end](#running-the-front-end)
  - [Running the Back-end](#running-the-back-end)
- [API Documentation](#api-documentation)
- [Testing](#testing)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

CRM-System is designed to streamline the process of managing customer relationships. It helps businesses organize their customer data, track sales progress, and generate insightful reports. The application is split into two major parts:

- **Frontend**: Developed using **React** to provide a dynamic, responsive user interface for managing customers, sales, and reports.
- **Backend**: Built with **Spring Boot**, which handles user authentication, customer management, sales tracking, and reporting features.

Key features of the CRM-System include:
- User authentication via **JWT**.
- Manage customer information, interactions, and sales activities.
- Sales tracking and reporting for business insights.
- Admin panel for managing users, customers, and sales data.
- Integration with external services like email notifications (optional).

---

## Tech Stack

### Front-end:
- **React** (v17+): For building the user interface with a component-based architecture.
- **React Router**: For handling navigation and routing.
- **Redux**: For state management.
- **Axios**: For making HTTP requests to the backend.
- **Material UI**: For building responsive and attractive UI components.
- **JWT Authentication**: Secure user authentication with JSON Web Tokens.

### Back-end:
- **Spring Boot** (v2.5+): For building the backend RESTful APIs.
- **Spring Security**: For JWT-based authentication and role-based access control.
- **Spring Data JPA**: For managing database interactions.
- **MySQL**: A relational database for data storage.
- **Swagger**: For API documentation and testing (optional).
- **JUnit**: For unit and integration testing.

### Other:
- **Docker**: For containerizing the application (optional).
- **Email Notification Integration** (optional): For sending customer-related emails (e.g., appointment reminders).

---

## Key Features

- **User Authentication**: 
  - Secure login and registration with JWT tokens for user authentication.
  - Role-based access control for admins and users.

- **Customer Management**: 
  - Add, edit, and delete customer profiles.
  - Track customer interactions and update information.

- **Sales Management**: 
  - Create and manage sales opportunities, track progress.
  - Assign sales reps to opportunities.

- **Reporting & Analytics**: 
  - Generate sales reports with filters (date range, sales rep, etc.).
  - Visualize sales data in charts.

- **Admin Dashboard**: 
  - Admin users can manage users, customers, and sales data.
  - View activity logs and generate reports.

---

## Frontend & Backend Repositories

You can find the **source code** for both the **frontend** and **backend** of the CRM-System platform at the following repository links:

- **Frontend Repository** (React):  
  [CRM-System Frontend](https://github.com/Ajay-Babare/StudentSystemAppReactFrontend)

- **Backend Repository** (Spring Boot):  
  [CRM-System Backend](https://github.com/Ajay-Babare/StudentSystemAppSpringBootBackEnd)

---

## Installation

### Front-end Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Ajay-Babare/StudentSystemAppReactFrontend.git
   cd StudentSystemAppReactFrontend
  

2. Install dependencies:
  `npm install`

3. Configure API URL in `src/config.js` (update to match your backend URL):
   ```javascript
   export const API_URL = 'http://localhost:8080/api';

5. Start the React development server:
  `npm start`

6. Access the front-end at:
   `http://localhost:3000/`.
---

### Back-end Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Ajay-Babare/StudentSystemAppSpringBootBackEnd.git
   cd StudentSystemAppSpringBootBackEnd

2. Install dependencies and build the project:
   `mvn clean install`

3. Configure database connection in `src/main/resources/application.properties`:
```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/studentsystem
   spring.datasource.username=root
   spring.datasource.password=password
   spring.jpa.hibernate.ddl-auto=update
   spring.security.jwt.secret=your-jwt-secret
```
4. Run the Spring Boot application:
   ```bash
   mvn spring-boot:run

5. Access the back-end at:
   `http://localhost:8080/`.
---
## Running the Application
### Running the Front-end
1. After setting up the front-end (as described above), run:
   ```bash
   npm start

2. Access the app in your browser at:
  `http://localhost:3000/`.
---
### Running the Back-end
1. After setting up the back-end (as described above), run:
   ```bash
   mvn spring-boot:run

2. Access the back-end at `http://localhost:8080/`
---
## API Documentation
   The back-end exposes the following API endpoints for communication with the front-end:

#### Authentication
   - **POST /api/auth/register**: Register a new user.
   - **POST /api/auth/login**: Log in and get a JWT token.

#### Customers
   - **GET /api/customers**: List all customers.
   - **POST /api/customers**: Add a new customer.
   - **PUT /api/customers/{id}**: Edit an existing customer.
   - **DELETE /api/customers/{id}**: Delete a customer.

#### Sales
   - **GET /api/sales**: List all sales opportunities.
   - **POST /api/sales**: Create a new sales opportunity.
   - **PUT /api/sales/{id}**: Update an existing sales opportunity.
   - **DELETE /api/sales/{id}**: Delete a sales opportunity.

#### Reports
   - **GET /api/reports/sales**: Generate sales report.

---

## Testing
- Unit Tests: Unit tests are included for both the front-end (using Jest) and back-end (using JUnit).
- Integration Testing: Use Postman or Swagger UI to test API endpoints.

---
## Deployment
### Dockerization
1. Dockerize the back-end: Create a Dockerfile in the back-end project and build the Docker image.
2. Dockerize the front-end: Similarly, you can containerize the react front-end if needed.
3. Deploy on Cloud: Use AWS, Google Cloud, or Heroku for scalable production deployment.
---
## Contributing
We welcome contributions to CRM-System! Here's how you can contribute:

1. Fork the repository.
2. Create a feature branch (git checkout -b feature/your-feature).
3. Make your changes and commit (git commit -m 'Add new feature').
4. Push your changes to your fork (git push origin feature/your-feature).
5. Open a pull request with a clear description of your changes.
---
## License
CRM-System is licensed under the MIT License. See the LICENSE file for more information.
