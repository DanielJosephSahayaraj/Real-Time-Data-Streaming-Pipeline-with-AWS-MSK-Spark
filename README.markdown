# Real-Time Data Streaming Pipeline with AWS MSK and Spark

## Overview
A scalable streaming pipeline that ingests simulated transaction data using **AWS MSK (Kafka)**, processes it with **Spark Streaming**, stores results in **S3**, and visualizes insights in **Power BI**.

## Architecture
1. **Producer** – Python script continuously publishes transaction data to MSK topic.
2. **Consumer** – PySpark Streaming application consumes messages in micro-batches and writes to S3.
3. **Storage** – Raw + processed data in S3.
4. **Orchestration** – AWS Lambda triggers additional processing/analytics.
5. **Visualization** – Power BI dashboard for business insights.

## Technologies
- **Streaming**: Apache Kafka, AWS MSK
- **Processing**: PySpark
- **Cloud**: AWS (S3, Lambda, VPC, IAM)
- **Languages**: Python, PySpark
- **Visualization**: Power BI

## Setup Instructions
1. Clone repo
2. Configure AWS MSK cluster + topic
3. Run producer: `python src/producer.py`
4. Run consumer: `spark-submit src/consumer_spark.py`
5. Deploy Lambda function

## Results
- Successfully implemented end-to-end streaming pipeline.
- Data flows from producer → MSK → Spark → S3.
- Built Power BI dashboard showing transaction patterns.

## Future Enhancements
- Add real-time anomaly detection ML model
- Integrate LLM for text analysis in stream
- Containerize with ECS/Fargate

GitHub: https://github.com/Danielmichaelraj/...
