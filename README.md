
# Weather Data ETL Pipeline with Apache Airflow

## Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline for weather data using Apache Airflow. The pipeline performs the following tasks:

1. **Data Extraction**: Fetches weather forecast data from the [WeatherAPI](https://www.weatherapi.com/).
2. **Data Transformation**: Converts JSON data to CSV format and performs additional data transformations.
3. **Data Loading**: Loads the transformed data into MySQL and NoSQL (MongoDB) databases.
4. **Data Archiving**: Archives raw and processed data files.
5. **Data Visualization**: Generates visualizations using Streamlit.

## Project Structure

- **DAGs**: Contains the Apache Airflow DAG (Directed Acyclic Graph) file (`weather_project.py`) defining the workflow.
- **Scripts**: Contains Python scripts for data extraction, transformation, and visualization.
- **Archive**: Directory for storing archived data files.
- **Logs**: Directory for storing logs generated during pipeline execution.

## Prerequisites

- Python 3.x
- Apache Airflow
- MySQL Server
- MongoDB
- Streamlit
- WeatherAPI API Key

## Setup and Installation

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/weather-data-etl.git
    ```

2. Install the required Python packages:

    ```bash
    pip install -r requirements.txt
    ```

3. Set up Apache Airflow, MySQL, MongoDB, and Streamlit as per your environment.

## Configuration

- Update the WeatherAPI API key in `weather_project.py`.
- Update database connection details in the respective Python scripts (`pyspark_sample.py`, `csv_conv.py`, `transform.py`).

## Usage

1. Start Apache Airflow scheduler:

    ```bash
    airflow scheduler
    ```

2. Trigger the `weather_project` DAG in the Apache Airflow UI or using the CLI.

3. Monitor the pipeline execution and check the logs for any errors.

## Contributing

Feel free to contribute to this project. Create a pull request with your changes, and they will be reviewed.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
