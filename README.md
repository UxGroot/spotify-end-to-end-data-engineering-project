# Spotify End-to-End Data Engineering Project
## Description
In this project, we will build an ETL (Extract, Transform, Load) pipeline using the Spotify API on AWS. In this we will retrieve data from the Spotify API, transform into a desired format, and load it into AWS data store.

### About Dataset/ API
This API contains information about music artist, albums, and songs - [Spotify API](https://developer.spotify.com/documentation/web-api)

### Services Used
1. **S3(Simple Storage Service):** Amazon S3 is a highly scalable object storage service that can store and retrieve any amount of data from anywhere on thr web. It is commonly used to store and distribute large media files data backups and static website files.
2. **AWS Lambda:** AWS Lambda is a serverless computing service that lets you run your code without managing servers. We can use Lambda to run the code in response to events like changes in S3, DynamoDB or other AWS services.
3. **CloudWatch:** Amazon ClodWatch is a monitoring service for AWS resources and the applications you run on them. We can use CloudWatch to collect and track metrics, collect and monitor log files, and set alarms.
4. **Glue Crawler** AWS Glue Crawler is a fully managed service that automatically crawls your data sorces , identifies data formats and infers schemas to create an AWS Glue Data Catalog.
5. **Data Catalog:** AWS Glue Data Catalog is a fully managed metadata repository that makes it easy to discover and manage data in AWS. We can use the Glue Data Catalog with other AWS services , such as Athena.
6. **Amazon Athena:** Amazon Athena is an interactive query service that makes it easy to analyse data in Amazon S3 using standard SQL. We can use Athena to analyse data in Glue Data Catalog or in other S3 bucket.

### Install Packages
```
pip install pandas
pip install numpy
pip install spotipy
```

### Project Execution Flow
Extract data from API -> Lambda Trigger (every 1 hour) -> Run Extract Code -> Store Raw Data -> Trigger Transform Function -> Transform Data and Load It -> Query Using Athena
