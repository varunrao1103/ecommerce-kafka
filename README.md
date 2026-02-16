# SpringBoot Kafka topic (Ecommerce)
## 📂 Modules
### 1️⃣ base-domains

Contains shared DTOs

OrderDto

OrderEvent

Used by producer and consumer services

### 2️⃣ order-service

REST API to create orders

Publishes OrderEvent to Kafka topic

Acts as Kafka Producer

### 3️⃣ email-service

Consumes OrderEvent from Kafka

Simulates sending email notification

Acts as Kafka Consumer

### 4️⃣ stock-service

Consumes OrderEvent from Kafka

Simulates stock validation/update

Acts as Kafka Consumer

### 🔄 Event Flow

Client sends order request to order-service

order-service publishes event to Kafka topic

email-service receives event and processes notification

stock-service receives event and updates stock

## 🛠 Technologies Used

Java 17

Spring Boot

Spring Kafka

Apache Kafka

Maven

REST APIs
