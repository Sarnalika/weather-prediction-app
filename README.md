##Weather Prediction Web App
This project implements a weather prediction web app that fetches live weather data using the OpenWeatherMap API and predicts future weather trends using machine learning. The app provides real-time weather information for any city around the world, along with a detailed forecast and a temperature prediction chart.

#Project Overview
The web app performs the following tasks:

Retrieves live weather data (temperature, humidity, wind speed, pressure, etc.) for any city.
Displays a forecast for the next few hours with temperature and humidity trends.
Trains a machine learning model using historical weather data to predict future weather conditions.
Uses regression to predict future temperature and humidity values.
Visualizes predictions with a temperature prediction chart.
##Features
Live Weather Data: Fetches current weather data from the OpenWeatherMap API.
Weather Forecast: Displays temperature, humidity, pressure, wind speed, and other conditions for the selected city.
Temperature Prediction: Shows predicted temperature trends for the next few hours.
Search Functionality: Allows users to search for weather data of any city around the world.
Setup and Installation
#Requirements
To run this project locally, make sure you have the following installed:

Python 3.x
Google Colab (for running the model and processing historical data)
Flask (for creating the web app)
Postman (for testing the OpenWeatherMap API requests)
#Installation Steps
Clone the repository:

bash
Copy
Edit
git clone https://github.com/yourusername/weather-prediction-app.git
cd weather-prediction-app
Install the required Python packages:

bash
Copy
Edit
pip install -r requirements.txt
#Get an API key from OpenWeatherMap:

Go to the OpenWeatherMap API website.
Sign up for an account and generate an API key.
Replace the placeholder API key in the code with your own key.
Run the web app:

bash
Copy
Edit
python app.py
Access the app:

#Open your browser and go to http://localhost:5000/ to access the app.
How It Works
1. Fetch Current Weather Data
The app fetches current weather data for any city by sending a GET request to the OpenWeatherMap API. The weather data includes temperature, humidity, wind speed, and more.

2. Machine Learning Model for Predictions
The app uses historical weather data (stored in a CSV file) to train a machine learning model. The model uses features like temperature, humidity, wind speed, and pressure to predict future weather conditions.

3. Predict Future Weather
Using regression techniques, the app predicts future temperature and humidity for the next few hours. The predictions are displayed as a visual chart.

4. Web Interface
The app allows users to search for the weather of any city worldwide. The weather information, including a temperature prediction chart, is displayed on the web page.

#Code Breakdown
1. Import Libraries
The project uses the following Python libraries:

requests for making API calls.
pandas for handling and analyzing historical data.
numpy for numerical operations.
sklearn for machine learning models and data preprocessing.
matplotlib for plotting temperature prediction charts.
2. Fetch Current Weather Function
This function uses the OpenWeatherMap API to fetch weather data for a specified city and returns the current temperature, humidity, wind speed, and other weather conditions.

3. Read Historical Data
The historical weather data is read from a CSV file and cleaned for use in training the machine learning model.

4. Train Machine Learning Model
The model is trained using historical weather data, and it uses classification for training and regression for predicting future weather values.

5. Predict Future Weather
The trained model is used to predict the temperature and humidity for the next 6 hours.

6. Web Interface
A simple web interface built using Flask allows users to search for any city and display the live weather data along with predictions.
