# Weather-Data-Pipeline-with-Airflow-and-AWS
Automated weather data pipeline using Airflow ; AWS: Extracts data from OpenWeather API, transforms with Python, stores in AWS S3. Airflow DAGs automate the process. Ideal for learning data orchestration ; integration with cloud services.

## Architecture

![openweatherapi_project_airflow](https://github.com/Atharv1604/Weather-Data-Pipeline-with-Airflow-and-AWS/assets/78715129/231c6c0f-6918-4c54-825b-46e13267cd6e)

The main goal was to automate the extraction, transformation, and storage of weather data. Let me break it down:

**Extraction**: I began by pulling weather data from the OpenWeather API. This API provides a wealth of information such as temperature, humidity, wind speed, and more. I used this data as a source for our project.

**OpenWeatherMapAPI Link** :- https://openweathermap.org/current

**OpenWeatherMapAPI Call** :- https://api.openweathermap.org/data/2.5/weather?q={city name}&appid={API key}

![image](https://github.com/Atharv1604/Weather-Data-Pipeline-with-Airflow-and-AWS/assets/78715129/b96ec617-dc19-4a13-9e58-4c5cae075df4)

**Transformation:** Once we had the raw data, I utilized Python to transform it according to our project's requirements. This could involve cleaning up the data, calculating additional metrics, or any other necessary manipulations to get it in the desired format.

**Storage:** The transformed data was then stored in an AWS S3 bucket. S3 is a highly scalable and reliable storage service provided by Amazon Web Services. Storing the data in S3 ensured durability and accessibility for downstream processes.

**Automation with Airflow:** To tie everything together and make the process fully automated, I created Directed Acyclic Graphs (DAGs) in Apache Airflow. Airflow is a platform to programmatically author, schedule, and monitor workflows. The DAGs I designed orchestrated the entire process: triggering the data extraction from OpenWeather API, running the Python transformations, and finally, storing the processed data in the S3 bucket.

**AIRFLOW Workflow Screenshot**

![photo_2024-04-05_11-14-10](https://github.com/Atharv1604/Weather-Data-Pipeline-with-Airflow-and-AWS/assets/78715129/f4c6bae4-bb72-4420-8f32-a4c7ce8c3c68)

**AWS S3 Bucket Screenshot**

![photo_2024-04-05_11-14-50](https://github.com/Atharv1604/Weather-Data-Pipeline-with-Airflow-and-AWS/assets/78715129/0bfca65e-6d6c-4e59-8c2d-3ad081b4e93e)

So, in essence, this project showcased the integration of various technologies to create an end-to-end automated data pipeline. We leveraged the OpenWeather API for data, Python for transformations, AWS S3 for storage, and Apache Airflow for workflow orchestration. This not only streamlined the process but also ensured reliability and scalability for handling weather data effectively.
