# Complete AWS Services Catalog

## Table of Contents

1. Compute Services
2. Storage Services
3. Database Services
4. AI/Machine Learning Services
5. Analytics Services
6. Security & Identity Services
7. Networking & Content Delivery Services
8. Management & Monitoring Services
9. Developer Tools
10. Application Integration Services

## Compute Services

- **Amazon Elastic Compute Cloud (EC2)**: Virtual servers in the cloud. Provides resizable compute capacity with various instance types optimized for different workloads. Supports multiple operating systems and integrates with other AWS services for complete infrastructure solutions.

- **AWS Lambda**: Serverless compute service that runs code in response to events. Automatically scales from a few requests per day to thousands per second with millisecond latency. Supports multiple programming languages and only charges for actual compute time consumed.

- **Amazon Elastic Container Service (ECS)**: Fully managed container orchestration service. Enables running and scaling containerized applications on AWS with support for both EC2 and Fargate launch types. Provides deep integration with AWS services for monitoring, security, and load balancing.

- **Amazon Elastic Kubernetes Service (EKS)**: Managed Kubernetes service for containerized applications. Automatically manages the Kubernetes control plane and worker nodes across multiple Availability Zones. Simplifies the deployment and management of Kubernetes applications.

- **AWS Fargate**: Serverless compute engine for containers. Eliminates the need to provision and manage servers while running ECS or EKS workloads. Automatically scales compute based on application demands and charges only for resources consumed.

- **AWS App Runner**: Fully managed service that makes it easy to deploy web applications and APIs at scale. Automatically builds and deploys web applications, with infrastructure management handled by AWS.

- **AWS Batch**: Fully managed batch processing service. Plans, schedules, and executes batch computing workloads across the full range of AWS compute services. Ideal for parallel processing of large-scale computing jobs.

- **Amazon Lightsail**: Simplified virtual private server (VPS) service. Provides easy-to-use compute, storage, and networking for simple web applications. Includes everything needed to get started quickly with predictable monthly pricing.

- **AWS Outposts**: Fully managed service that extends AWS infrastructure and services to virtually any on-premises facility. Enables consistent hybrid cloud architecture with AWS APIs and tools.

- **AWS Local Zones**: Infrastructure deployments that place compute, storage, database, and other select AWS services closer to large population centers. Provides single-digit millisecond latency for latency-sensitive applications.

## Storage Services

- **Amazon Simple Storage Service (S3)**: Industry-leading scalable object storage. Offers various storage classes for cost optimization and includes features like versioning, lifecycle policies, and encryption. Commonly used for backup, static website hosting, and data lakes.

- **Amazon S3 Glacier**: Long-term data archival service with multiple retrieval options:

  - Glacier Instant Retrieval: Millisecond retrieval for archive data
  - Glacier Flexible Retrieval: Minutes to hours retrieval time
  - Glacier Deep Archive: Lowest cost for rarely accessed data

- **Amazon S3 Express One Zone**: High-performance object storage for latency-sensitive applications. Delivers consistent single-digit millisecond latency and high throughput. Ideal for machine learning training, media processing, and real-time analytics.

- **Amazon Elastic Block Store (EBS)**: High-performance block storage for EC2 instances. Provides multiple volume types optimized for different workloads and automatically replicates within Availability Zones. Supports point-in-time snapshots for backup and migration.

- **Amazon Elastic File System (EFS)**: Fully managed elastic NFS file system. Automatically scales storage capacity and performance based on demand. Supports concurrent access from thousands of compute instances with consistent low latency.

- **Amazon FSx**: Family of fully managed file systems:

  - FSx for Windows File Server: Native Windows file system
  - FSx for Lustre: High-performance computing
  - FSx for OpenZFS: Cost-effective ZFS file system
  - FSx for NetApp ONTAP: Enterprise data management

- **AWS Storage Gateway**: Hybrid cloud storage integration service. Provides seamless integration between on-premises applications and AWS cloud storage. Supports file, volume, and tape gateway configurations.

- **AWS Snow Family**: Physical edge computing and data transfer devices:
  - Snowcone: Small, rugged edge computing
  - Snowball Edge: Petabyte-scale data transport
  - Snowmobile: Exabyte-scale data transfer

## Database Services

- **Amazon Relational Database Service (RDS)**: Managed relational database service supporting multiple engines (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB). Automates administration tasks like hardware provisioning, database setup, patching, and backups.

- **Amazon Aurora**: MySQL and PostgreSQL-compatible database engine delivering up to 5x performance. Automatically grows storage from 10GB to 128TB and replicates data across multiple Availability Zones. Includes serverless option for variable workloads.

- **Amazon DynamoDB**: Fully managed NoSQL database service delivering consistent single-digit millisecond performance. Automatically scales throughput and storage while maintaining performance at any scale. Features global tables, backups, and encryption.

- **Amazon ElastiCache**: Fully managed in-memory caching service supporting Redis and Memcached. Enables sub-millisecond latency for real-time applications. Simplifies deployment and management of distributed caching environments.

- **Amazon Redshift**: Fully managed data warehouse service for analyzing large datasets. Enables analyzing exabyte-scale data using standard SQL and existing business intelligence tools. Provides built-in compression and columnar storage.

- **Amazon DocumentDB**: MongoDB-compatible document database service. Scales compute and storage independently while maintaining MongoDB compatibility. Provides automated backups and point-in-time recovery.

- **Amazon Neptune**: Graph database service optimized for storing billions of relationships. Supports popular graph models including Property Graph and RDF. Enables millisecond latency graph queries.

- **Amazon Timestream**: Purpose-built time series database for collecting and processing time-series data. Automatically scales compute and storage to handle billions of daily events.

- **Amazon Keyspaces**: Managed Apache Cassandra-compatible service. Provides scalable, highly-available, and managed Cassandra-workload capabilities with encryption and backup.

## AI/Machine Learning Services

- **Amazon Bedrock**: Managed service for foundation models and generative AI. Provides unified API access to leading AI models with customization capabilities. Maintains security and compliance standards.

- **Amazon SageMaker**: Comprehensive machine learning platform. Includes tools for data labeling, feature engineering, model training, optimization, and deployment. Supports automated model tuning and production deployment.

- **Amazon CodeWhisperer**: AI-powered code generation service. Provides real-time code suggestions based on natural language comments and existing code. Supports multiple programming languages and IDEs.

- **Amazon Rekognition**: Computer vision and image analysis service. Identifies objects, people, text, scenes, and activities in images and videos. Provides facial analysis and recognition capabilities.

- **Amazon Comprehend**: Natural language processing service. Extracts insights from unstructured text using machine learning. Identifies entities, key phrases, sentiment, and topic modeling.

- **Amazon Q**: Generative AI-powered business intelligence service. Enables natural language queries across organizational data with AI-generated insights while maintaining security standards.

- **Amazon Polly**: Text-to-speech service using deep learning. Converts text to lifelike speech in multiple languages and voices. Supports custom lexicons and SSML.

- **Amazon Transcribe**: Automatic speech recognition service. Converts audio to text with high accuracy. Supports multiple languages and custom vocabularies.

- **Amazon Textract**: OCR and document analysis service. Extracts text, forms, and tables from documents. Maintains formatting and relationships between data.

- **Amazon Forecast**: Time series forecasting service combining statistical and machine learning approaches. Provides accurate predictions for business metrics and planning.

- **Amazon Personalize**: Real-time personalization and recommendation service. Creates custom ML models for personalized user experiences. Integrates with existing applications.

## Analytics Services

- **Amazon EMR (Elastic MapReduce)**: Managed big data platform. Processes vast amounts of data using open-source tools such as Apache Spark, Hive, and Presto. Automatically scales resources and handles cluster management.

- **Amazon Kinesis**: Platform for streaming data on AWS:

  - Kinesis Data Streams: Real-time data streaming
  - Kinesis Data Firehose: Data delivery to AWS services
  - Kinesis Data Analytics: Real-time analytics
  - Kinesis Video Streams: Video ingestion and processing

- **Amazon Athena**: Interactive query service for S3 data. Enables analyzing data directly in S3 using standard SQL without moving the data. Serverless operation with pay-per-query pricing.

- **Amazon QuickSight**: Cloud-native business intelligence service. Delivers interactive dashboards and ML-powered insights. Provides embedded analytics capabilities.

- **Amazon OpenSearch Service**: Distributed search and analytics suite. Enables real-time application monitoring, log analytics, and full-text search. Built on open-source OpenSearch.

- **AWS Glue**: Serverless data integration service. Provides ETL capabilities and data catalog. Supports both batch and streaming data processing.

- **Amazon DataZone**: Data management and governance service. Enables data discovery, sharing, and access control. Maintains data governance standards.

- **AWS Clean Rooms**: Secure data collaboration service. Enables privacy-safe data analysis between parties. Supports customizable collaboration rules.

- **Amazon MSK (Managed Streaming for Apache Kafka)**: Fully managed Apache Kafka service. Provides secure and scalable streaming infrastructure. Supports native Kafka tools.

## Security & Identity Services

- **AWS Identity and Access Management (IAM)**: Global security service managing access to AWS resources. Controls authentication and authorization for users and applications. Provides fine-grained permissions management.

- **Amazon GuardDuty**: Intelligent threat detection service. Continuously monitors AWS accounts and workloads for malicious activity. Uses machine learning to identify threats.

- **AWS Shield**: Managed DDoS protection service. Provides always-on detection and automatic inline mitigations. Available in Standard and Advanced tiers.

- **AWS Web Application Firewall (WAF)**: Web application firewall service. Protects web applications from common exploits and bots. Includes customizable security rules.

- **Amazon Macie**: Data security and privacy service. Uses machine learning to discover and protect sensitive data. Provides automated sensitive data discovery.

- **AWS Key Management Service (KMS)**: Managed cryptographic key service. Creates and controls encryption keys with centralized management. Integrates with AWS services.

- **AWS Certificate Manager**: SSL/TLS certificate management service. Provisions, manages, and deploys certificates. Integrates with AWS services.

- **AWS Secrets Manager**: Secrets management service. Rotates, manages, and retrieves database credentials, API keys, and other secrets. Enforces encryption.

- **Amazon Detective**: Security investigation service. Analyzes security findings and identifies root causes. Uses machine learning for behavior analytics.

- **AWS IAM Identity Center**: Centralized access management service. Manages SSO access to multiple AWS accounts and applications. Integrates with corporate directories.

## Networking & Content Delivery Services

- **Amazon Virtual Private Cloud (VPC)**: Isolated cloud networks. Provides complete control over the virtual networking environment. Includes selection of IP ranges, subnets, routing tables, and gateways.

- **Amazon CloudFront**: Global content delivery network. Securely delivers data, videos, applications, and APIs with low latency. Integrates with AWS Shield for DDoS protection.

- **Amazon Route 53**: Scalable domain name system service. Provides highly available and scalable DNS, domain registration, and health checking. Supports various routing policies.

- **Amazon API Gateway**: Managed service for creating and maintaining APIs. Handles all tasks involved in accepting and processing API calls. Includes traffic management and monitoring.

- **AWS Direct Connect**: Dedicated network connection service. Provides consistent network experience with reduced costs. Supports hybrid cloud architecture.

- **AWS Transit Gateway**: Network transit hub service. Connects VPCs and on-premises networks. Simplifies network architecture.

## Management & Monitoring Services

- **Amazon CloudWatch**: Monitoring and observability service. Provides data and insights for AWS resources, applications, and services. Includes metrics collection, log analytics, and automated actions.

- **AWS Systems Manager**: Operations and application management service. Provides unified interface for managing AWS resources. Includes automation, parameter store, and session management.

- **AWS CloudTrail**: Governance, compliance, and audit service. Records API activity and events in AWS accounts. Enables security analysis and compliance auditing.

- **AWS CloudFormation**: Infrastructure as code service. Allows modeling and provisioning AWS resources using templates. Supports automatic rollback and drift detection.

- **AWS Config**: Resource inventory and configuration service. Tracks AWS resource inventory and changes. Enables security analysis and resource administration.

- **AWS Control Tower**: Account governance service. Sets up and governs multi-account AWS environments. Implements compliance controls and best practices.

## Developer Tools

- **AWS CodeCatalyst**: Unified software development service. Provides integrated environment for planning, coding, building, and deploying applications. Includes project management features.

- **AWS Cloud9**: Cloud-based IDE. Enables writing, running, and debugging code from a web browser. Includes pre-configured development environments.

- **AWS CodeCommit**: Managed source control service. Hosts secure Git repositories. Supports collaboration features and integrates with other AWS developer tools.

- **AWS CodeBuild**: Continuous integration service. Compiles code, runs tests, and produces deployment packages. Supports multiple languages and build types.

- **AWS CodeDeploy**: Automated deployment service. Coordinates application deployments to compute services. Supports EC2, Lambda, and on-premises servers.

- **AWS CodePipeline**: Continuous delivery service. Automates build, test, and deployment phases. Integrates with source control and third-party tools.

- **AWS X-Ray**: Application monitoring and debugging service. Analyzes and debugs distributed applications. Provides request tracing and performance insights.

- **AWS Amplify**: Full-stack application development platform. Simplifies building, deploying, and hosting applications. Includes pre-built UI components and backend services.

## Application Integration Services

- **Amazon EventBridge**: Serverless event bus service. Connects applications using events. Enables building event-driven architectures at scale.

- **Amazon Simple Notification Service (SNS)**: Managed pub/sub messaging service. Enables high-throughput message delivery to subscribing endpoints. Supports multiple protocols including HTTP/S, email, and SMS.

- **Amazon Simple Queue Service (SQS)**: Managed message queuing service. Enables decoupling and scaling of distributed applications. Supports standard and FIFO queues with guaranteed message delivery.

- **AWS Step Functions**: Visual workflow service for distributed applications. Coordinates multiple AWS services into serverless workflows. Provides automatic scaling and error handling.

- **AWS AppSync**: Managed GraphQL service. Simplifies application data access and updates. Supports real-time data synchronization.

- **Amazon MQ**: Managed message broker service. Supports Apache ActiveMQ and RabbitMQ. Provides enterprise messaging capabilities with high availability.

- **AWS AppFlow**: SaaS integration service. Automates bidirectional data flows between AWS and SaaS applications. Includes pre-built connectors for popular services.
