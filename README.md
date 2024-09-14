I made this project for Sydney to help with her daily commute to class! I deployed this on PythonAnywhere and automated the process using the scheduled task feature.

# Weather-Based Calendar Notification System
This project is a Python-based application that integrates with Google Calendar, OpenWeatherMap, and OpenAI's GPT-3.5 to provide personalized weather-based recommendations for upcoming events.

## Features
Fetches upcoming events from Google Calendar
Retrieves weather forecast data for a specified location
Generates custom messages using OpenAI's GPT-3.5
Sends SMS notifications with event details, weather information, and personalized messages

## Prerequisites
Before you begin, ensure you have met the following requirements:

Python 3.6+
Google Cloud Console project with Calendar API enabled
OpenWeatherMap API key
OpenAI API key
Textbelt API key (for SMS functionality)

## Installation

1. Clone this repository:
> Copygit clone https://github.com/plaussermair/syd-commute.git
> cd syd-commute

2. Install the required packages:
>pip install -r requirements.txt

3. Set up your environment variables by creating a .env file in the project root:
   - OPENWEATHER_API_KEY=your_openweather_api_key
   - OPENAI_API_KEY=your_openai_api_key
   - TEXTBELT_API_KEY=your_textbelt_api_key
   - PHONE_NUMBER=your_phone_number }

5. Set up Google Calendar API:
   - Create a project in Google Cloud Console
   - Enable the Google Calendar API
   - Create OAuth 2.0 credentials (download as client_secret.json and place in the project root)

## Usage
Run the main script:
>python google_calendar.py

The script will:
1. Check for upcoming events in your Google Calendar
2. Fetch weather data for the specified location
3. Generate a custom message with event details, weather information, and additional content
4. (Optional) Send an SMS with the generated message

## Configuration

Modify the latitude and longitude in google_calendar.py to set your desired location for weather forecasts.
Adjust the time range for upcoming events in get_calendar_events() function.

## Contributing
Contributions to this project are welcome. Please fork the repository and create a pull request with your changes.

## Disclaimer
This project is for educational purposes only. Ensure you comply with the terms of service for all APIs used in this project.
