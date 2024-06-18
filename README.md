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

**Functionalities:**

**- Create Contact:** Allows users to add new contact records.

**- Retrieve Contact:** Fetches contact information based on user requests.

**- Update Contact:** Enables users to modify existing contact details.

**- Delete Contact:** Removes contact records as requested by users.

**How It Works:** When a client needs to perform operations on contacts, the API Gateway routes the request to the Contact Service. The Contact Service processes the request and returns the relevant data or updates.

**4. API Gateway Service**

**Purpose:** The API Gateway Service acts as the entry point for client applications and centralizes requests to various microservices. It can handle authentication, load balancing, and routing.

**Functionalities:**

**- Request Routing:** Receives incoming requests from clients and routes them to the appropriate microservice based on the request path or URL.

**- Authentication:** Manages user authentication for incoming requests.

**- Load Balancing:** Distributes requests among multiple instances of a service to balance the load.

**- Cross-cutting Concerns:** Handles other concerns such as logging, rate limiting, and security.

**How It Works:**

The API Gateway serves as the single-entry point for external clients (e.g., web or mobile applications) to interact with the microservices. It routes client requests to the appropriate microservices, handles authentication, and addresses other cross-cutting concerns.

# Architecture Overview

These microservices work together to create a modular and scalable architecture. Each microservice has its own specific area of responsibility, making it easier to develop, test, and maintain. The API Gateway Service provides a unified API while handling cross-cutting concerns such as authentication and load balancing.

Eureka Server ensures that microservices can dynamically discover and communicate with each other, allowing for flexibility in scaling and maintaining the system. This microservices architecture promotes agility, scalability, and the ability to deploy and update individual components independently, ultimately leading to a more resilient and maintainable system.

# How the microservices will communicate with each other?

<img width="500" alt="ContactHub " src="https://github.com/sanaya-bhardwaj/ContactHub-Contact_management_system/assets/135012941/2a171101-ee0c-466e-8546-6ed039177781">

• API Gateway is the entry point for client requests.

• Eureka (Service Registry) registers and tracks microservices.

• User Service manages user-related data.

• Contact Service handles contact-related data.

• API Gateway routes client requests to the appropriate service.

• Eureka enables services to discover each other.

• User Service handles user data and operations.

• Contact Service manages contact data.

• Services communicate via HTTP-based RESTful APIs.

# Cloud Platform Selection 

• **Java Ecosystem Support:**

➢ *AWS* has excellent support for Java applications, making it well-suited for a project built on the Spring Boot framework.

➢ *AWS* offers services like *AWS Elastic Beanstalk* and *AWS Lambda*, which are particularly useful for deploying and managing Java applications.

• **Microservices Architecture:**

➢ AWS provides a range of services that support microservices architecture, such as *Amazon ECS (Elastic Container Service)* and *AWS Lambda*.

➢ Integration with *AWS API Gateway* can help in creating and managing APIs for the microservices.

• **Scalability and Flexibility:**

➢ AWS provides scalable solutions through services like *Amazon EC2* for virtual servers and Amazon RDS for managed databases.

➢ Auto Scaling features can automatically adjust capacity based on demand.

• **Extensive Service Offering:**

➢ AWS has a comprehensive set of services, including databases *(Amazon DynamoDB, Amazon RDS)*, *storage (Amazon S3), and messaging (Amazon SQS)*, which are crucial for a microservices architecture.

# Container Orchestration

**DEPLOYMENT STEPS:**

• Containerizing Microservices with Docker

• Building Docker Images

• Pushing Docker Images to Container Registry

• Deploying Microservices with Kubernetes

• Creating Kubernetes Deployments using commands:

- *kubectl apply -f deployment-service1.yaml*
  
- *kubectl apply -f deployment-service2.yaml*
  
• Creating Kubernetes Services using commands:

- kubectl apply -f service-service1.yaml

- kubectl apply -f service-service2.yaml
