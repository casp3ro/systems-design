# Define Use Cases & Gather Requirements

## Understand the Problem & Scope

Before designing the system, it is critical to clearly define its purpose, users, and functional boundaries. This ensures alignment between expectations and the final architecture.

## Define Use Cases

- Collaborate with the interviewer to define the primary use cases.
- Suggest additional features that might enhance the system.
- Identify and remove features that are out of scope, as determined by the interviewer.
- Assume high availability is a required feature and explicitly include it in the use cases.

## Clarifying Questions

To gain complete context and ensure precise requirements, ask key questions:

- Who are the users of the system?
- How will they interact with it?
- What functionality does the system provide?
- What are the expected inputs and outputs?

## Categorizing Requirements

- **Crucial Requirements**: Features essential for the system’s core functionality and expected to be implemented from the start.
- **Non-Crucial Requirements**: Additional features or optimizations that enhance the system but are not mandatory in the first iteration.

# Constraints

Understanding system constraints is critical for designing a scalable and efficient architecture. The following factors must be determined:

## Traffic & User Load

- **Total Users**: Estimated number of users registered in the system.
- **Daily Active Users (DAU)**: Percentage of users interacting with the system daily.
- **Concurrent Users**: Peak number of users accessing the system simultaneously.

## Request Volume & Ratios

- **Total Requests per Month** (ask explicitly).
- **Requests per Second (RPS)**:
  - Read requests per second.
  - Write requests per second.
- **Read-to-Write Ratio**: Typically estimated using the 80/20 rule (80% reads, 20% writes) unless specified otherwise.

## Data Storage & Growth

- **Types of Data**: Define a basic schema for stored data (structured/unstructured).
- **Data Ingestion Rate**:
  - Amount of new data written per second.
  - Expected storage growth over time.
- **Storage Requirements**:
  - How much data is stored per day/month/year.
  - Total storage required over 5 years.
- **Data Retention**: Duration for which historical data must be preserved.

## Performance Considerations

- **Latency**: Acceptable response time for read and write operations.
- **Throughput**: Maximum number of requests the system can handle per second.
- **Bandwidth Estimates**: Expected data transfer requirements based on storage and user requests.

# Abstract Design / High-Level Design

## High-Level Components

Main Components: Sketch out key components of the system like:

- User Interface (UI)
- API Gateway
- Services (like authentication, data processing)
- Database
- Caching Layer (optional for performance)

## Justify Design Decisions

Explain why each component is needed.  
Example: Chose a relational database for structured data or a NoSQL database for flexibility and scalability.

## Key Components to Focus On

Pick 2-3 major parts to discuss in more detail based on the system's needs. Example:

- **API Logic**: How the API processes requests.
- **Key Algorithms**: Briefly describe important operations (e.g., caching or load balancing).

## Basic Database Schema

Outline the core tables (e.g., users, orders) and how they relate.  
Mention important indexes for faster lookups (e.g., `user_id`, `timestamp`).

## Basic API Design

Example API Endpoints:

- `POST /users`: Create a user
- `GET /users/{id}`: Get user info
- `PUT /users/{id}`: Update user info
- `DELETE /users/{id}`: Delete a user

# Low-Level Design with Availability, Reliability, and Scaling

## Key Characteristics of Distributed Systems

A distributed system must focus on the following key characteristics to ensure proper operation:

- **Scalability**: The system can handle increased load by adding more resources (horizontal/vertical scaling).
- **Reliability**: The system operates as expected, even when there are failures.
- **Availability**: The system remains accessible even during failures.
- **Efficiency**: The system can perform operations efficiently, maintaining good resource usage.
- **Manageability**: The system is easy to monitor, troubleshoot, and scale.

## Layers in the System

The system is typically designed in layers for better management and scalability:

- **Service Layer**: Handles business logic and user interactions.
- **Data Layer**: Manages storage, ensuring data consistency, durability, and retrieval.
- **Caching Layer**: Reduces load on the database by temporarily storing frequently accessed data.

## Infrastructure Components

- **Load Balancing**: Distributes traffic across multiple servers to avoid overloading a single server.
- **Messaging/Queueing Systems**: Ensures smooth communication between services, particularly in asynchronous systems.

## Horizontal vs. Vertical Scaling

- **Horizontal Scaling (Scaling out)**: Adding more machines or instances to the system. Ideal for increasing capacity without affecting performance.
- **Vertical Scaling (Scaling up)**: Increasing the resources (CPU, RAM) of existing machines. Typically used when it's not feasible to add more machines.

## Fault Tolerance & Replication

- **Fault Tolerance**: Ensures the system continues functioning despite failures in individual components.
- **Replication**: Copies of data are stored across different servers to ensure data availability and reduce the risk of data loss.

## CAP Theorem

The **CAP Theorem** explains the trade-offs between the three key properties in a distributed system:

- **Consistency (C)**: All nodes have the same data at any point in time.
- **Availability (A)**: Every request receives a response (either success or failure).
- **Partition Tolerance (P)**: The system can handle network partitions, where some nodes can't communicate with others.

The theorem states that a distributed system can achieve at most two of these three properties at any given time.

## PACELC Theorem

The **PACELC Theorem** extends the CAP Theorem to cover scenarios when there is no partition:

- **P**: Partition.
- **A**: Availability.
- **C**: Consistency.
- **L**: Latency.
- **E**: Else (when no partition).

In the absence of a partition, the system can trade off between Latency (L) and Consistency (C).

## ACID Properties

For databases, especially relational databases, it’s important to maintain **ACID properties**:

- **Atomicity**: All operations in a transaction are completed, or none are.
- **Consistency**: The database transitions from one valid state to another.
- **Isolation**: Transactions don’t affect each other, even if executed concurrently.
- **Durability**: Once a transaction is committed, it’s permanent, even in the case of system failure.

# Detailed Core Component Design

When designing the core components of the system, the following elements play a crucial role. Each component needs to be carefully selected and configured to meet the system’s scalability, availability, and reliability requirements.

## Base Components

### App - Client

The client is the interface where users interact with the system, typically through a web or mobile application. It communicates with the backend via API calls. Key aspects to consider:

- Frontend frameworks (e.g., React, Angular)
- Authentication and authorization mechanisms (e.g., JWT tokens, OAuth)

### API - Server

The API server is responsible for processing requests from clients and interacting with the backend components (e.g., database, caching, etc.). Consider:

- REST APIs: Standard for simple CRUD operations.
- GraphQL: Flexible and allows clients to request specific data.
- tRPC: Type-safe APIs that eliminate the need for separate client-server API schemas.
- Rate limiting: Prevents abuse by restricting the number of requests a user can make.

### Database (SQL/NoSQL)

The database stores the data. The choice between SQL and NoSQL depends on the data structure and requirements:

- **SQL**: Best for structured, relational data (e.g., MySQL, PostgreSQL).
- **NoSQL**: Suitable for unstructured or semi-structured data (e.g., MongoDB, Cassandra).
- **Replicas**: Multiple copies of the database can ensure high availability and load balancing.
- **Sharding**: Splitting the database into smaller chunks (shards) to distribute data across different servers for scalability.

### Caching

Caching improves read performance by temporarily storing frequently accessed data. Consider using:

- In-memory caching (e.g., Redis, Memcached)
- Distributed caching for scaling.
- Cache eviction policies (e.g., LRU, LFU) to manage cache size.

### Load Balancer

A load balancer distributes incoming requests across multiple servers to ensure that no single server is overwhelmed. Types of load balancing strategies include:

- Round-robin: Distributes requests equally.
- Least connections: Routes requests to the server with the least active connections.
- Weighted: Assigns weights to servers based on their capacity.

### Queue

Queues handle asynchronous operations by placing tasks in a queue and processing them in the background. This helps decouple components and ensures smooth operation.

- Message queues (e.g., RabbitMQ, Kafka, SQS) to manage event-driven architectures.
- Task queues (e.g., Celery) for background task processing.

### Storage

For storing large files (e.g., images, videos, documents), consider:

- Object storage (e.g., AWS S3, Google Cloud Storage)
- Block storage: For databases or virtual machines.

### Content Delivery Network (CDN)

A CDN speeds up content delivery by caching content closer to users geographically. Use a CDN (e.g., Cloudflare, AWS CloudFront) to:

- Distribute static assets like images, videos, and stylesheets globally.
- Improve load times and reduce latency.

### Proxies

Proxies can act as intermediaries for API calls, adding an extra layer of security and control. Consider using:

- Reverse proxies (e.g., Nginx, HAProxy) to route traffic to appropriate backend servers.
- API Gateway to manage, throttle, and route API calls.

## Replication & Sharding

- Replication ensures high availability by maintaining copies of data across multiple servers.
- Sharding distributes data across different servers or databases to ensure scalability. This can be done based on data partitions like user ID or geographic region.

## Pooling/Streaming/Events

- **Pooling**: For managing and reusing connections or resources (e.g., database connection pools).
- **Streaming**: Handles real-time data processing (e.g., Kafka, AWS Kinesis).
- **Event-driven architecture**: Enables asynchronous communication between services, with events triggering actions.

## Monitoring & Health Checks

- **Monitoring**: Continuously track the health, performance, and usage of system components (e.g., Datadog, Prometheus, Grafana).
- **Health Checks**: Implement health checks to ensure that services are running properly and can recover from failures automatically. This helps in proactive failure management.
  - **Liveness checks**: Ensure services are running.
  - **Readiness checks**: Ensure services are ready to accept traffic.

# Bottlenecks & Additional Considerations

## Common Bottlenecks & Solutions

### Increased Number of Read Requests

- **Problem**: High read traffic can overload the database or APIs.
- **Solution**:
  - Cache frequently accessed data (e.g., with Redis).
  - Use read replicas to distribute the load.

### Scaling the Database

- **Problem**: As data grows, the database may slow down.
- **Solution**:
  - Sharding: Split data into smaller parts (e.g., by user ID) to distribute it across multiple servers.
  - Replicas: Use replicas to spread read traffic.

### Unexpected Traffic Spikes

- **Problem**: Sudden increases in traffic can overwhelm the system.
- **Solution**:
  - Auto-scaling: Automatically add resources when needed (e.g., cloud auto-scaling).
  - Load balancing: Distribute traffic evenly across servers.
  - Rate limiting: Control the number of requests users can make.

## Other Key Considerations

### Network Latency

- **Problem**: Network delays can affect performance, especially with distributed systems.
- **Solution**:
  - Use CDNs to cache content closer to users.
  - Deploy services regionally to reduce distance and latency.

### API Overload

- **Problem**: Too many requests can slow down APIs.
- **Solution**:
  - Rate limiting to control how many requests users can make in a given time.
  - Retry logic to handle occasional failures.

### Database Locking

- **Problem**: Simultaneous access to data can cause delays.
- **Solution**:
  - Use optimistic locking to reduce contention.
  - Partition data to avoid too many simultaneous accesses to the same part.

# Communication in System Design Interviews

## Gathering System Requirements

When gathering requirements, ask the right questions to ensure you fully understand the system. Be clear and methodical to cover the following:

### User Details:

- How many active users will the system support?
- Where are users located (geographically)?
- What kind of devices will users access the system from?

### Traffic and Usage Patterns:

- What are the expected number of requests per second (both read and write)?
- Are there any peak usage times or patterns we should know about?

### Data Handling:

- What kind of data will be stored (e.g., user profiles, transactions)?
- What is the expected growth rate of data (per second or per month)?

Be sure to clarify the crucial vs. non-crucial requirements so you know what to prioritize.

## Explaining Design Decisions

When presenting your design, always explain your reasoning clearly:

- Start with the high-level design before diving into specific components.
- Justify each design choice: For example, explain why you chose a certain database type (SQL vs. NoSQL) or caching mechanism (e.g., Redis) based on requirements like scalability or low-latency needs.
- Discuss trade-offs and potential alternatives: For instance, "I considered using a single database for everything, but scaling reads became a challenge, so I opted for read replicas."
- Be transparent about compromises: Explain if you had to make a choice between consistency and availability (e.g., using a NoSQL database with eventual consistency for better availability).

## Explaining Alternatives and Thought Process

It’s important to show you’ve thought through multiple design options and can justify your choices:

- Talk about alternatives:
  - "We could use a monolithic architecture, but microservices would scale better in the long run."
- Walk through the reasoning:
  - "By sharding the database by user region, we can distribute traffic evenly and improve read latency."
- Discuss trade-offs:
  - "Using a caching layer like Redis can improve performance but adds complexity in terms of cache invalidation."

## Engaging with the Interviewer

To ensure you're on the right track, involve the interviewer in the conversation:

- Ask for feedback:
  - "Does this approach seem reasonable to you? Is there something you would change?"
- Clarify your assumptions:
  - "I’m assuming that we want low-latency reads and can tolerate eventual consistency. Does that align with the requirements?"
- Get validation:
  - After explaining a key decision, ask for the interviewer’s thoughts:
    - "I’m considering using a NoSQL database due to its scalability for unstructured data. Do you agree with this choice, or would you suggest an alternative?"

## Clear and Unambiguous Communication

When explaining your design:

- Be concise: Stick to the most relevant details and avoid unnecessary jargon.
- Use diagrams and sketches: A visual representation of your design helps make abstract concepts clearer.
- Focus on clarity: Always ensure your ideas are easy to follow by breaking down complex decisions into simple explanations.
- Stay calm and logical: If you encounter a challenging question, calmly walk through your thought process rather than rushing to an answer.
