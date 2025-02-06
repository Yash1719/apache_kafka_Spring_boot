# Publisher-Subscriber Model using Spring Boot and Zookeeper

This guide will help you set up and run a Publisher-Subscriber model using Spring Boot and Kafka.

### Prerequisites

Before we begin, ensure you have the following installed:

- Java (JDK 8 or later)
- Maven
- Apache Kafka
- Spring Boot (you can use Spring Initializr to generate your Spring Boot application)

### Steps to Set Up Kafka

1. **Download and Install Kafka**
   - Visit the official Kafka website: [Kafka Quickstart](https://kafka.apache.org/quickstart)
   - Download the latest Kafka version for your operating system and extract it.

2. **Start Zookeeper**
   - Open a command prompt and navigate to your Kafka installation directory:
     ```sh
     D:\kafka_2.13-3.9.0
     ```
   - Run the following command to start Zookeeper:
     ```sh
     bin\windows\zookeeper-server-start.bat config\zookeeper.properties
     ```

3. **Start Kafka Server**
   - In a new command prompt window, navigate to the same Kafka installation directory and run the following command to start Kafka:
     ```sh
     bin\windows\kafka-server-start.bat config\server.properties
     ```

### Kafka Producer and Consumer

Once Kafka and Zookeeper are running, you can start sending and consuming messages.

#### 1. **Running Kafka Producer**

- Open a command prompt and run the following command to start the Kafka producer:
  ```sh
  .\bin\windows\kafka-console-producer.bat --topic topic1 --bootstrap-server localhost:9092
  >This is my first event
  >This is my second event


#### 2. **Running Kafka Consumer**

- Open another command prompt and run the following command to start the Kafka consumer:
  ```sh
  .\bin\windows\kafka-console-consumer.bat --topic topic1 --from-beginning --bootstrap-server localhost:9092
  
The consumer will begin consuming messages from the Kafka topic topic1 from the beginning (if available).

### **Terminating Kafka**
To stop Kafka and Zookeeper, press Ctrl+C in the respective command prompt windows where Kafka and Zookeeper are running.
