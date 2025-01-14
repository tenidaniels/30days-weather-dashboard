# Weather Data Collection System(Day 1) - 30 Days DevOps Challenge(tenidaniels)

Welcome to the **Weather Data Collection System**! This project is part of the **30 Days DevOps Challenge**, where the goal is to build a weather data collection system that showcases core DevOps principles.  

## 🚀 Features  

- Fetches **real-time weather data** for multiple cities.  
- Displays key details: **temperature (°F)**, **humidity**, and **weather conditions**.  
- Automatically stores weather data in **AWS S3** for secure storage.  
- Supports tracking **multiple cities** simultaneously.  
- Timestamps all weather data for historical tracking.  

## 🛠️ Tech Stack  

- **Language**: Python 3.x  
- **Cloud Provider**: AWS (S3)  
- **External API**: OpenWeather API  
- **Dependencies**:  
  - `boto3` (AWS SDK)  
  - `python-dotenv` (Environment management)  
  - `requests` (HTTP requests)  

## 📂 Project Structure  

  ```plaintext
weather-dashboard/
    src/
        __init__.py
        weather_dashboard.py
    tests/
    data/
    .env
    .gitignore
    requirements.txt
```

## 🚀 Getting Started
Follow these steps to set up and run the project locally:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/tenidaniels/30days-weather-dashboard.git
    cd 30days-weather-dashboard
    ```

2. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3. **Configure environment variables:**

    Create a `.env` file in the root of the project with the following values:

    ```bash
    OPENWEATHER_API_KEY=your_api_key_here
    AWS_BUCKET_NAME=your_s3_bucket_name_here
    ```

    - You can retrieve your **OpenWeather API Key** by signing up at [OpenWeather API](https://openweathermap.org/api).
    - For **AWS S3**:
      - Create an S3 bucket in AWS (name it according to the value of `AWS_BUCKET_NAME`).
      - Ensure you have configured AWS CLI with valid credentials using `aws configure`.

4. **Run the application:**
    ```bash
    python3 src/weather_dashboard.py
    ```

    The script will fetch the weather data for predefined cities, process it, and save it to your AWS S3 bucket.

### 📊 Sample Output
```
Fetching weather for Philadelphia... Temperature: 28.87°F Feels like: 16.75°F Humidity: 44% Conditions: scattered clouds Successfully saved data for Philadelphia to S3

Fetching weather for Seattle... Temperature: 48.97°F Feels like: 46.58°F Humidity: 84% Conditions: clear sky Successfully saved data for Seattle to S3

Fetching weather for New York... Temperature: 27.03°F Feels like: 14.43°F Humidity: 42% Conditions: few clouds Successfully saved data for New York to S3
```

## 🧠 What I’ve Learned

During this project, I learned a lot about:

- **AWS S3**: I got hands-on experience in creating and managing S3 buckets for cloud storage.
- **Environment Variable Management**: I learned how to securely manage sensitive information, like API keys, using `.env` files.
- **Python Best Practices**: From writing clear and maintainable Python code to implementing proper error handling when interacting with external APIs and cloud services.
- **Git**: I followed a simple version control workflow using Git, ensuring I tracked changes effectively.






