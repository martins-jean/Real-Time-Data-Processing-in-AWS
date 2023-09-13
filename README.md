# Real-time data processing in AWS

## Contextual overview

The administration of a city would like to improve the efficiency of its wind farms and anticipate possible defects in wind turbines due to excessively high wind speeds. They would like to know when wind speeds get severe so that they can quickly alert maintenance teams and dispatch them where needed. 

## Architecture diagram

## Project objectives

1. To collect and process streaming data, we will use Amazon Kinesis Data Streams.
2. To analyze the data from the data stream, we will use Amazon Kinesis Data Analytics for Apache Flink. We can author and run an Apache Flink application against streaming sources to detect higher than normal wind speeds.
3. Configure an external destination to send the output data. We can use an AWS Lambda function to take the data and store it in an Amazon DynamoDB table, which is an ideal service for scenarios where low latency is required.
4. To alert the maintenance team when an anomaly occurs, we can create a second Lambda function to scan and filter the DynamoDB table for anomaly records, and then publish a notification to an Amazon SNS topic and get real-time alerts when there is an anomaly.

## Reproducibility guidelines
