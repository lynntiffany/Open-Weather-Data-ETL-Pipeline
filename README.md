# Weather Data ETL Pipeline

## 1. Project Overview

This project demonstrates a basic ETL (Extract, Transform, Load) pipeline using real-time weather data from the OpenWeather API.

The pipeline extracts weather data for three cities — Nairobi, London, and Dubai — transforms the raw API responses into a structured dataset using Pandas, and stores the processed data in a CSV file for analysis.

The project also performs basic analysis and visualization to compare temperature, humidity, wind speed, and weather conditions across the selected cities.

## 2. Data Source

**OpenWeather API**

The OpenWeather API was used to retrieve current weather information for:

* Nairobi
* London
* Dubai

The following fields were collected:

| Field             | Description                     |
| ----------------- | ------------------------------- |
| City              | Name of the city                |
| Temperature       | Temperature in degrees Celsius  |
| Humidity          | Relative humidity percentage    |
| Weather Condition | Current weather description     |
| Wind Speed        | Wind speed in metres per second |
| Date and Time     | Time of data extraction         |

## 3. ETL Process

### Extract

The `Requests` library was used to connect to the OpenWeather API and retrieve weather data for the three selected cities.

The API returned the weather information as raw JSON responses.

### Transform

The raw API responses were transformed into a structured Pandas DataFrame.

The transformation process included:

* Selecting the required weather fields.
* Creating clear and descriptive column names.
* Converting the API timestamp into a readable date and time format.
* Organizing the data into a tabular structure.
* Checking data types.
* Checking for missing values.
* Checking for duplicate records.

No missing values or duplicate records were identified in the extracted dataset, so no additional cleaning was required.

### Load

The transformed dataset was saved as a CSV file named:

`weather_data.csv`

The processed file can be used for further analysis without having to repeat the transformation process.

## 4. Tools Used

* **Python** — Used to develop the ETL pipeline.
* **Requests** — Used to connect to the OpenWeather API and extract data.
* **Pandas** — Used for data transformation, cleaning, and analysis.
* **Matplotlib** — Used to create visualizations.
* **Jupyter Notebook** — Used to develop and document the project.
* **OpenWeather API** — Used as the weather data source.
* **CSV** — Used to store the processed dataset.

## 5. Steps Taken

1. Created an OpenWeather API account and generated an API key.
2. Connected Python to the OpenWeather API using the Requests library.
3. Selected Nairobi, London, and Dubai as the cities for data collection.
4. Extracted weather data from the API for each city.
5. Inspected the raw JSON responses.
6. Selected the required fields from the API responses.
7. Structured the extracted information into a Pandas DataFrame.
8. Renamed and organized the columns into a clear format.
9. Converted the API timestamp into a readable date and time format.
10. Checked the dataset for missing values and duplicates.
11. Saved the transformed dataset as `weather_data.csv`.
12. Compared temperature, humidity, wind speed, and weather conditions across the three cities.
13. Created visualizations to communicate the results.
14. Documented the ETL process and findings.

## 6. Key Findings

The analysis of the collected weather data produced the following findings:

* **Dubai recorded the highest temperature** at **37.96°C**, while Nairobi recorded the lowest at **14.93°C**.
* **Nairobi recorded the highest humidity** at **100%**, while Dubai recorded the lowest at **44%**.
* **Dubai recorded the strongest wind speed** at **6.17 m/s**, while Nairobi recorded the lowest at **3.09 m/s**.
* Nairobi and London recorded **overcast clouds**, while Dubai recorded **broken clouds**.
* The results demonstrate noticeable differences in weather conditions across the three cities at the time of data extraction.

> **Note:** The findings represent weather conditions at the time the API data was collected and should not be interpreted as long-term climate patterns.
