# Digital Bank Microservices

Welcome to the **Digital Bank Microservices** project! This is a modern, scalable, and secure banking system built with **Java**, **Spring Boot**, and other microservices technologies. The system is designed to demonstrate real-world banking functionalities while incorporating innovative features such as **fraud detection** and **dynamic credit scoring** using **machine learning**.

## Features

### Core Services
- **Customer Service**: Manages customer registration and profile details.
- **Account Service**: Handles the creation of accounts and their balance operations (deposit, withdrawal).
- **Transaction Service**: Manages all transaction-related activities, including inter-account transfers and transaction history.
- **Loan Service**: Allows users to apply for loans and manage repayment schedules.
- **Fraud Detection Service**: Real-time fraud detection using machine learning (TensorFlow or Weka) based on transaction patterns.
- **Credit Scoring Service**: Dynamically evaluates the creditworthiness of customers using data from transactions, spending patterns, and external sources.
- **Notification Service**: Sends notifications (email, SMS, push) for account activities, fraud alerts, and loan approvals.

## Key Technologies Used
- **Spring Boot**: For building RESTful microservices.
- **Spring Cloud**: For service discovery (Eureka), API Gateway (Spring Cloud Gateway), and centralized configuration (Spring Cloud Config).
- **Spring Security**: For authentication and authorization with JWT.
- **Kafka/RabbitMQ**: For event-driven communication (e.g., notifications, fraud detection events).
- **Machine Learning**: TensorFlow/Weka for fraud detection and credit scoring.
- **MySQL/PostgreSQL**: For relational database management (customer, account, transaction data).
- **MongoDB**: For storing non-relational data like transaction logs.
- **Docker**: For containerizing the application.
- **Prometheus & Grafana**: For monitoring microservices and application health.
- **ELK Stack**: For centralized logging and log analysis.

## Microservices Architecture

The **Digital Bank** is broken down into several independent microservices:

1. **Customer Service** - Handles customer profiles and registration.
2. **Account Service** - Manages bank accounts.
3. **Transaction Service** - Manages transactions like deposits, withdrawals, and transfers.
4. **Loan Service** - Manages loan applications and approvals.
5. **Fraud Detection Service** - Uses machine learning models to detect fraudulent transactions.
6. **Credit Scoring Service** - Provides dynamic credit scoring for customers.
7. **Notification Service** - Handles customer notifications for all banking activities.

Each service runs independently and communicates with other services through **REST APIs** and **event-driven messaging**.

## Installation

To run the **Digital Bank** locally or on a cloud platform, follow these steps:

### Prerequisites:
- **Java 11** or later
- **Docker** (for containerization)
- **MySQL/PostgreSQL** for relational database (Dockerized or local)
- **MongoDB** (Dockerized or local)
- **Kafka** or **RabbitMQ** for event-driven architecture

### Steps to run the project:

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/digital-bank-microservices.git
   cd digital-bank-microservices
   
2. Docker Compose: To quickly set up all the services (database, Kafka, etc.) with Docker Compose, run:

```bash
Copy code
docker-compose up --build
```

3. Configure application properties:

Update the application properties for each service (in src/main/resources/application.properties) to match your environment, such as database credentials, message broker configurations, etc.

4. Run the application: Navigate to each service directory and use Maven/Gradle to run the services:

For example:

```bash
Copy code
mvn spring-boot:run
```
Or for Dockerized services, simply use docker-compose as above.

5. Access the API:

After starting the services, access the API documentation through Swagger (configured in each service).
Example: http://localhost:8080/swagger-ui.html (for Customer Service)

## Sample Data:
- Use the following sample data for testing purposes (you can find it in the data folder).
- Example POST requests can be tested through Swagger UI or Postman.
  
## API Documentation

Swagger-based API documentation is available for each service. After starting the service, you can access it by navigating to:

- Customer Service: http://localhost:8081/swagger-ui.html
- Account Service: http://localhost:8082/swagger-ui.html
- Transaction Service: http://localhost:8083/swagger-ui.html
- Loan Service: http://localhost:8084/swagger-ui.html
- Fraud Detection Service: http://localhost:8085/swagger-ui.html
- Notification Service: http://localhost:8086/swagger-ui.html
  
## Features to Explore
**Fraud Detection:** Test the fraud detection service by simulating suspicious transactions. You can see how transactions are analyzed in real-time for fraud.
**Loan Application** Apply for a loan and see how the system evaluates your creditworthiness using the dynamic credit scoring service.
**Transaction History** View the transaction history and balances in the Account Service.
**Notifications:** Test the notification service to receive alerts for successful transactions, fraud detection alerts, and loan approvals.
  
## Future Enhancements
**Blockchain Integration:** Add blockchain-based transaction verification for added security and immutability.
**AI Chatbot:** Integrate a chatbot for customer service using AI to help customers check balances, apply for loans, etc.
**Kubernetes Deployment:** Containerize all microservices and deploy them to a Kubernetes cluster for easier scaling and management.

## Contributing

We welcome contributions to improve this project! If you'd like to contribute, follow these steps:

1. Fork the repository.
2. Clone your fork to your local machine.
3. Create a new branch (git checkout -b feature-name).
4. Make your changes and commit (git commit -am 'Add new feature').
5. Push to the branch (git push origin feature-name).
6. Submit a pull request.
   


## Contact
For questions, feedback, or collaboration - poorvaja.sathasivam@outlook.com


