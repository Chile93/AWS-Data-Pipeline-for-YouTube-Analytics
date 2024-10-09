# AWS Data Pipeline for YouTube Analytics 🚀

This project demonstrates the design and implementation of a scalable, serverless data pipeline on **AWS** to process and analyze YouTube data. The architecture leverages **AWS Glue**, **S3**, **Athena**, **Lambda**, and **QuickSight** to deliver insights into YouTube video trends, such as views, likes, comments, and more.

## Table of Contents
- [Architecture Overview](#architecture-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Data Flow](#data-flow)
- [Setup and Installation](#setup-and-installation)
- [Visualization Dashboard](#visualization-dashboard)
- [Contributing](#contributing)
- [License](#license)

## Architecture Overview

<img src="Architecture.jpg">

The architecture consists of several AWS services working together to process data in real time:

- **Data Ingestion**: YouTube data is extracted using an API and stored in the **S3 Landing Area**.
- **Data Processing**: **AWS Glue** is used to cleanse, transform, and enrich the data before storing it in an **Enriched S3** bucket.
- **Data Querying**: **AWS Athena** is utilized to query data directly from S3 for further analysis.
- **Data Visualization**: The data is visualized using **AWS QuickSight** to create interactive dashboards, presenting insights on video views, likes, dislikes, and more.
- **Automation**: **AWS Lambda** and **Step Functions** are used to orchestrate the ETL processes.
- **Monitoring**: The entire architecture is monitored with **AWS CloudWatch** for real-time alerts and performance tracking.

## Features

- **Scalable**: The solution is fully serverless and scales automatically to handle large volumes of YouTube data.
- **Real-time Processing**: Automates data collection and transformation using **Lambda** and **Glue**.
- **Custom Dashboards**: Leverage **AWS QuickSight** for powerful data visualizations and insights.
- **Automated Orchestration**: **AWS Step Functions** manage and coordinate the entire data pipeline workflow.
- **Monitoring and Alerts**: **CloudWatch** ensures the system's reliability with alerts for failures or performance issues.

## Technologies Used

- **AWS S3**: Data storage.
- **AWS Glue**: ETL processing.
- **AWS Lambda**: Function execution.
- **AWS Athena**: Data querying.
- **AWS QuickSight**: Data visualization and dashboard creation.
- **AWS CloudWatch**: System monitoring and alerting.
- **AWS Step Functions**: Workflow orchestration.

## Data Flow

1. **Data Collection**: YouTube data (video_id, views, likes, comments, etc.) is pulled using the YouTube API and stored in **S3**.
2. **ETL Process**: **AWS Glue** performs transformations (cleansing, aggregation) on the data, outputting results into the **Cleansed/Enriched** bucket.
3. **Querying**: The processed data is queried using **AWS Athena** to derive insights like trends in views, likes, and other user engagement metrics.
4. **Visualization**: Data is displayed in **AWS QuickSight** dashboards, offering visual insights into trends such as the top-performing videos and categories.
5. **Automation**: **AWS Lambda** and **Step Functions** automatically manage data collection and processing without manual intervention.

## Setup and Installation

### Prerequisites
- **AWS Account** with access to S3, Glue, Lambda, Athena, and QuickSight.
- **YouTube API Key** for fetching video data.
- Python 3.x for writing Lambda functions.

### Steps

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-username/YouTube-AWS-Data-Pipeline.git
    cd YouTube-AWS-Data-Pipeline
    ```

2. **Configure AWS CLI**:
    Ensure AWS CLI is installed and configured with the appropriate permissions.

    ```bash
    aws configure
    ```

3. **Deploy AWS Resources**:
   - Create S3 buckets for data storage.
   - Set up **AWS Glue** jobs for data transformation.
   - Create **AWS Lambda** functions for automation.
   - Enable **AWS Athena** to query processed data.
   - Build **AWS QuickSight** dashboards for visual insights.

4. **Schedule Data Processing**:
   Use **AWS Step Functions** to automate daily/weekly data processing workflows.

5. **Visualize Data**:
   Set up dashboards in **AWS QuickSight** to display YouTube trends, such as:
   - Top 10 videos by views
   - Engagement metrics (likes, comments, dislikes)
   - Video performance by category and channel.

## Visualization Dashboard

Here’s an example of a **QuickSight Dashboard**:

![QuickSight Dashboard Screenshot](link-to-dashboard-image)

## Contributing

Feel free to fork the repository and submit pull requests! Contributions are welcome.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
