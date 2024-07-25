# Architect Assignment

## Project Overview
The monolithic application includes a feature for processing exchange orders on various crypto exchanges (Binance, Kraken, Bitstamp, etc.). Currently, the exchange record with corresponding attributes is being created in the database from various parts of the monolith application, then being processed in the background. The task is to design the architecture for extracting this functionality into a separate microservice while ensuring the system remains functional, scalable, and maintainable.

## Current Monolithic Architecture

### Database Schema
The relevant portion of the database schema for the ExchangeOrder includes the following table:

#### exchange_orders
- id
- orderable_id
- orderable_type
- category
- exchange_id
- status
- amount
- rate
- provider_order_id
- response
- from_currency_id
- to_currency_id
- exchange_status
- fee_amount
- order_type

## Assignment Requirements

### Deliverable
Provide a detailed architectural design document that includes the following components:

### Architecture Overview
- High-level architecture diagram showing the transition from a monolithic to a microservices architecture.
- Identification of the main components and their interactions.

### Microservice Design
- Detailed design of the ExchangeOrder microservice, including its responsibilities and how it will interact with the existing monolith.
- Database design for the new microservice.

### Communication Protocol
- Explanation of the chosen communication protocol (e.g., REST, gRPC, Kafka, RabbitMQ) between the microservices and the monolith.
- Justification for the chosen protocol, considering factors such as performance, scalability, and reliability.

### Data Consistency and Transactions
- Strategy for managing distributed transactions and ensuring data consistency across the monolith and the microservices.
- Explanation of eventual consistency and how it will be implemented if applicable.

### Monitoring and Logging
- Design for centralized logging and monitoring of the microservices.
- Tools and techniques for monitoring the health and performance of the microservices (e.g., ELK Stack, Prometheus, Grafana).

### Security Considerations
- Approach to securing communication between the monolith and the microservices.
- Authentication and authorization mechanisms for the microservices.