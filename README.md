### Real-Time Data Streaming Pipeline with Kafka, Airflow, Spark, and Docker
Overview
This project demonstrates the development of a real-time data streaming pipeline using modern data engineering tools such as Apache Kafka, Apache Airflow, Apache Spark, and Docker. The pipeline is designed to ingest, process, and store data extracted from an external API. To showcase the results, a Power BI dashboard was created to visualize key insights derived from the processed data.

The system architecture follows a scalable, distributed design to ensure fault-tolerance, efficient data processing, and ease of deployment.

System Architecture
The architecture for the pipeline is depicted below:
<img width="1171" alt="image" src="https://github.com/user-attachments/assets/8be586ad-6a50-4d75-bc14-ce01f077f43b">

Key Components:
API Data Source:
Random user data is extracted from an external API to simulate real-time streaming scenarios.

Apache Airflow:
Orchestrates the entire pipeline by scheduling and managing workflows. It triggers the ingestion of data from the API and sends it to Kafka for streaming.

Apache Kafka:
Acts as the central messaging system for streaming data. Kafka brokers stream data from producers (Airflow) to multiple consumers (Spark and other systems).

Apache Spark:
Processes streaming data in real time. It transforms and cleans the data for analysis and visualization.

Apache Cassandra:
A NoSQL database used for storing processed data. It ensures high availability and scalability for real-time read/write operations.

Docker:
Docker containers are used to deploy all services in a consistent and isolated environment.

Power BI:
Visualizes key metrics and insights extracted from the processed data for better decision-making.

Features
Real-Time Data Ingestion: API data is continuously fetched and streamed to Kafka.
Data Processing with Spark: Spark handles real-time transformations and analytics on the streamed data.
Orchestrated Pipelines: Airflow schedules and monitors the entire process.
Scalable Infrastructure: Dockerized services ensure easy scalability and portability.
Visualization with Power BI: Processed data is visualized to uncover actionable insights.
Project Workflow
Data Ingestion:

Random user data is fetched from an external API via Airflow DAGs.
Data is pushed to Kafka topics for streaming.
Data Streaming:

Kafka brokers stream the ingested data to consumers such as Spark.
Data Processing:

Spark processes the data for cleaning, transformation, and enrichment.
Data Storage:

Processed data is stored in Cassandra for future queries and visualization.
Data Visualization:

A Power BI dashboard connects to the processed data to display metrics such as user demographics, activity trends, and more.
