# ContactHub - Contact Management System

**Introduction**

In an increasingly interconnected world, managing personal and professional contacts efficiently is vital. ContactHub - The Contact Manager Microservices project leverages the power of Spring Boot, a robust Java-based framework, to create a scalable and highly maintainable solution for contact management.

# Microservices Design 

**1. User Service**

**Purpose:** The User Service is responsible for managing user-related data and authentication. It handles user registration, login, and user profile management.

**Functionalities:**

**- User Registration:** Allows new users to register and create an account.

**- Authentication:** Manages user login and authentication tokens.

**- Profile Management:** Enables users to view and update their profile information.

**How It Works:** When a client sends a request to the API Gateway that requires user-related information or actions, the API Gateway forwards the request to the User Service. The User Service processes the request and responds to the API Gateway.

**2. Contact Service**

**Purpose:** The Contact Service is focused on managing contact-related data. It handles the creation, retrieval, modification, and deletion of contact records.

