# Ingest Search

The project is a log ingestor and query interface system designed to handle large volumes of log data efficiently and provide a simple querying mechanism. The system uses various technologies to manage, store, and query logs, ensuring scalability and reliability.

## Components and Technologies Used

### Log Ingestor

- **Node.js and Express Server:**

  - Manages incoming HTTP requests.
  - Handles log ingestion and query responses.

- **RabbitMQ Message Queue:**

  - Receives logs and forwards them to a message queue.
  - Ensures logs are not lost and can be processed asynchronously.

- **MongoDB (Sharded):**

  - Stores log data efficiently.
  - Uses sharding (splitting data across multiple servers) for scalability.
  - Indexes timestamps for optimized write performance.

### Load Balancing

- **Nginx:**

  - Distributes incoming requests across multiple Node.js servers.
  - Ensures high availability and scalability by balancing the load.

### Query Interface

- **HTML Form:**

  - Provides a user-friendly interface for querying logs.
  - Accessible via a web browser at http://localhost:3000/.

- **GET Requests:**

  - Allows querying logs using URL parameters.
  - Examples include filtering logs by error level or specific messages.

- **Containerization:**
  - Docker is used to manage different images and containers.
  - Docker Compose simplifies multi-container Docker applications.

![image] (https://github.com/Sumitsh28/images/blob/2c79c673f7354ddbeff5abc33024719b0bcbaffe/ingestion.png?raw=true)
![image] (https://raw.githubusercontent.com/Sumitsh28/images/424bdedb72f050f2729adf43272e12e685ee7d8e/post.png)
![image] (https://raw.githubusercontent.com/Sumitsh28/images/424bdedb72f050f2729adf43272e12e685ee7d8e/get.png)
