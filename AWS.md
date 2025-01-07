# Amazon Web Services (AWS) - Complete Service Catalog

## Compute Services

- **Amazon Elastic Compute Cloud (EC2)**: Virtual servers in the cloud. Provides resizable compute capacity with various instance types optimized for different workloads. Supports multiple operating systems and integrates with other AWS services for complete infrastructure solutions.

- **AWS Lambda**: Serverless compute service that runs code in response to events. Automatically scales from a few requests per day to thousands per second with millisecond latency. Supports multiple programming languages and only charges for actual compute time consumed.

- **Amazon Elastic Container Service (ECS)**: Fully managed container orchestration service. Enables running and scaling containerized applications on AWS with support for both EC2 and Fargate launch types. Provides deep integration with AWS services for monitoring, security, and load balancing.

- **Amazon Elastic Kubernetes Service (EKS)**: Managed Kubernetes service for containerized applications. Automatically manages the Kubernetes control plane and worker nodes across multiple Availability Zones. Simplifies the deployment and management of Kubernetes applications.

- **AWS Fargate**: Serverless compute engine for containers. Eliminates the need to provision and manage servers while running ECS or EKS workloads. Automatically scales compute based on application demands and charges only for resources consumed.

- **AWS Batch**: Fully managed batch processing service. Plans, schedules, and executes batch computing workloads across the full range of AWS compute services. Ideal for parallel processing of large-scale computing jobs.

- **Amazon Lightsail**: Simplified virtual private server (VPS) service. Provides easy-to-use compute, storage, and networking for simple web applications. Includes everything needed to get started quickly with predictable monthly pricing.

## Storage Services

- **Amazon Simple Storage Service (S3)**: Scalable object storage with industry-leading durability. Offers various storage classes for cost optimization and includes features like versioning, lifecycle policies, and encryption. Commonly used for backup, static websites, and data lakes.

- **Amazon Elastic Block Store (EBS)**: High-performance block storage for EC2 instances. Provides multiple volume types optimized for different workloads and automatically replicates within Availability Zones. Supports point-in-time snapshots for backup and migration.

- **Amazon S3 Express One Zone**: High-performance object storage designed for latency-sensitive applications. Delivers consistent single-digit millisecond latency and high throughput. Ideal for machine learning training, media processing, and real-time analytics workloads.

- **Amazon Elastic File System (EFS)**: Fully managed elastic NFS file system. Automatically scales storage capacity and performance based on demand. Supports concurrent access from thousands of compute instances with consistent low latency.

- **Amazon FSx**: Family of fully managed file systems. Includes FSx for Windows File Server, FSx for Lustre, FSx for OpenZFS, and FSx for NetApp ONTAP. Each optimized for specific workload requirements and compatibility needs.

- **AWS Storage Gateway**: Hybrid cloud storage integration service. Provides seamless integration between on-premises applications and AWS cloud storage. Supports file, volume, and tape gateway configurations for different use cases.

## Database Services

- **Amazon Relational Database Service (RDS)**: Managed relational database service supporting multiple engines (MySQL, PostgreSQL, Oracle, SQL Server, MariaDB). Automates time-consuming administration tasks like hardware provisioning, database setup, patching, and backups. Provides high availability with Multi-AZ deployments.

- **Amazon DynamoDB**: Fully managed NoSQL database service delivering consistent single-digit millisecond performance. Automatically scales throughput and storage while maintaining performance at any scale. Features include global tables, point-in-time recovery, and encryption at rest.

- **Amazon Aurora**: MySQL and PostgreSQL-compatible relational database engine. Delivers up to 5x performance of MySQL and 3x of PostgreSQL with better availability. Automatically grows storage from 10GB to 128TB and replicates data across multiple Availability Zones.

- **Amazon ElastiCache**: Fully managed in-memory caching service. Supports Redis and Memcached engines for real-time applications requiring sub-millisecond latency. Simplifies deployment and management of distributed caching environments.

- **Amazon Redshift**: Fully managed data warehouse service. Enables analyzing large datasets using standard SQL and existing business intelligence tools. Provides built-in compression and columnar storage for query optimization.

- **Amazon DocumentDB (with MongoDB compatibility)**: Fully managed document database service. Compatible with MongoDB workloads while providing the scalability and durability of AWS. Automatically scales compute and storage independently.

- **Amazon Neptune**: Fully managed graph database service. Optimized for storing billions of relationships and querying the graph with milliseconds latency. Supports popular graph models including Property Graph and RDF.

- **Amazon Timestream**: Fully managed time series database service. Purpose-built for collecting, storing, and processing time-series data. Automatically scales storage and compute to handle billions of daily events.

## Artificial Intelligence/Machine Learning Services

- **Amazon Bedrock**: Managed service for foundation models and generative AI. Provides unified API access to top-performing models from leading providers. Enables customization and fine-tuning while maintaining security and compliance standards.

- **Amazon SageMaker**: Comprehensive machine learning platform. Includes tools for data labeling, feature engineering, model training, optimization, and deployment. Supports automated model tuning and production deployment with continuous monitoring.

- **Amazon CodeWhisperer**: AI-powered code generation service. Provides real-time code suggestions based on natural language comments and existing code. Supports multiple programming languages and integrates with popular IDEs.

- **Amazon Rekognition**: Computer vision and image analysis service. Identifies objects, people, text, scenes, and activities in images and videos. Provides highly accurate facial analysis, face comparison, and face search capabilities.

- **Amazon Comprehend**: Natural language processing (NLP) service. Extracts insights and relationships from unstructured text using machine learning. Identifies entities, key phrases, sentiment, and topic modeling.

- **Amazon Q**: Generative AI-powered business intelligence service. Enables natural language queries across organizational data sources. Provides AI-generated insights while maintaining enterprise security and compliance standards.

## Analytics Services

- **Amazon EMR (Elastic MapReduce)**: Managed big data platform. Processes vast amounts of data using open-source tools such as Apache Spark, Hive, HBase, and Presto. Automatically scales resources and handles cluster management.

- **Amazon Kinesis**: Platform for streaming data on AWS. Includes services for real-time data collection, processing, and analysis. Supports video streams, data streams, data firehose, and data analytics.

- **Amazon Athena**: Interactive query service for S3 data. Enables analyzing data directly in S3 using standard SQL without moving the data. Serverless operation means you pay only for queries you run.

- **Amazon QuickSight**: Cloud-native business intelligence service. Delivers interactive dashboards and ML-powered insights. Provides embedded analytics capabilities and pay-per-session pricing model.

- **Amazon OpenSearch Service**: Distributed search and analytics suite. Enables real-time application monitoring, log analytics, and full-text search. Built on open-source OpenSearch and OpenSearch Dashboards.

## Security & Identity Services

- **AWS Identity and Access Management (IAM)**: Global security service for AWS resources. Manages access to AWS services and resources securely. Controls authentication and authorization for users and applications.

- **Amazon GuardDuty**: Intelligent threat detection service. Continuously monitors AWS accounts, workloads, and data for malicious activity. Uses machine learning to identify threats and unexpected behavior.

- **AWS Shield**: Managed Distributed Denial of Service (DDoS) protection service. Provides always-on detection and automatic inline mitigations. Available in Standard (free) and Advanced tiers.

- **AWS Web Application Firewall (WAF)**: Web application firewall service. Protects web applications from common exploits and bots. Includes rules for SQL injection, cross-site scripting, and other vulnerabilities.

- **Amazon Macie**: Data security and privacy service. Uses machine learning to discover and protect sensitive data. Provides automated sensitive data discovery and continuous monitoring.

## Networking & Content Delivery Services

- **Amazon Virtual Private Cloud (VPC)**: Isolated cloud networks. Provides complete control over the virtual networking environment. Includes selection of IP ranges, subnets, route tables, and gateways.

- **Amazon CloudFront**: Global content delivery network (CDN). Securely delivers data, videos, applications, and APIs with low latency and high transfer speeds. Integrates with AWS Shield for DDoS protection.

- **Amazon Route 53**: Scalable domain name system (DNS) web service. Provides highly available and scalable DNS, domain registration, and health checking. Supports various routing policies including latency-based routing.

- **Amazon API Gateway**: Fully managed service for creating and maintaining APIs. Handles all tasks involved in accepting and processing API calls. Includes traffic management, monitoring, and API version control.

## Management & Monitoring Services

- **Amazon CloudWatch**: Monitoring and observability service. Provides data and insights for AWS resources, applications, and services. Includes metrics collection, log analytics, and automated actions.

- **AWS Systems Manager**: Operations and application management service. Provides a unified interface for managing AWS resources. Includes automation, parameter store, and session management.

- **AWS CloudTrail**: Governance, compliance, and audit service. Records API activity and events in AWS accounts. Enables security analysis, resource change tracking, and compliance auditing.

- **AWS CloudFormation**: Infrastructure as code service. Allows modeling and provisioning AWS resources using templates. Supports automatic rollback and drift detection.

## Developer Tools

- **AWS CodeCatalyst**: Unified software development service. Provides integrated environment for planning, coding, building, and deploying applications. Includes project management and collaboration features.

- **AWS Cloud9**: Cloud-based integrated development environment (IDE). Enables writing, running, and debugging code from a web browser. Includes pre-configured development environments.

- **AWS CodeCommit**: Fully managed source control service. Hosts secure Git repositories. Supports collaboration features and integrates with other AWS developer tools.

- **AWS Amplify**: Full-stack application development platform. Simplifies building, deploying, and hosting web and mobile applications. Includes pre-built UI components and ready-to-use backends.

## Application Integration Services

- **Amazon EventBridge**: Serverless event bus service. Connects applications using events. Enables building event-driven architectures at scale.

- **Amazon Simple Notification Service (SNS)**: Managed pub/sub messaging service. Enables high-throughput message delivery to subscribing endpoints. Supports multiple protocols including HTTP/S, email, and SMS.

- **Amazon Simple Queue Service (SQS)**: Fully managed message queuing service. Enables decoupling and scaling of distributed applications. Supports standard and FIFO queues with guaranteed message delivery.

- **AWS Step Functions**: Visual workflow service for distributed applications. Coordinates multiple AWS services into serverless workflows. Provides automatic scaling, error handling, and state management.
