# Weather Web App

A simple and responsive **Weather Web App** that lets users search for any city and view the current weather, along with a 4-day forecast. It displays key weather information such as temperature, weather conditions, humidity, wind speed, and more.

---

## Installation

Follow these steps to run the app on your local machine.

### Prerequisites

- A **web browser** (e.g., Chrome, Firefox, Safari, etc.)
- A **text editor** (e.g., Visual Studio Code, Sublime Text) for editing the code (optional)

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/weather-web-app.git
   ```

2. **Navigate to the project directory**:
   ```bash
   cd weather
   ```

3. **Open the `index.html` file** in your browser:
   You can open the file directly in your browser. Alternatively, you can use a local server for development.

---

## Usage

1. **Search for a city**:
   - Type the city name into the input field and click the search button (represented by a magnifying glass icon).
   - Alternatively, press `Enter` after typing the city name.

2. **View weather details**:
   - After a city is searched, the app will display the following details:
     - **Current temperature** (°C)
     - **Weather condition** (e.g., Clear, Clouds, Thunderstorm, etc.)
     - **Humidity** (%)
     - **Wind speed** (m/s)

3. **View the 4-day weather forecast**:
   - The app will show the 4-day forecast with temperature and weather icons for each day.

---

## Functionality Overview

### 1. **HTML Structure**:
The app uses a simple HTML structure with an input field to search cities and display weather data. Key sections in the HTML are:
- **Search input and button**: Users enter a city name and search for weather information.
- **Weather info section**: Displays current weather details like temperature, humidity, and wind speed.
- **Forecast section**: Shows the 4-day weather forecast with icons and temperatures.

### 2. **CSS Styling**:
The **CSS** file styles the app with a modern, minimal design:
- The background image is set to a weather-related backdrop, and a subtle gradient overlay is applied.
- A responsive design is implemented, with flexbox ensuring that the layout adapts to different screen sizes.
- Weather icons are placed next to the weather details for a visually appealing UI.

### 3. **JavaScript Logic**:
The **JavaScript** file handles the dynamic functionality of the app. Here are the key functions:

- **Event Listeners**:
  - `searchBtn` and `cityInput` both trigger the `updateWeatherInfo` function when clicked or when `Enter` is pressed, respectively.

- **`getFetchData()`**:
  - This function makes an API request to **OpenWeatherMap** using the provided city name and API key. It fetches the current weather and 7-day forecast data.
  
- **`getWeatherIcon()`**:
  - Based on the weather condition ID from the API, this function returns the corresponding icon (e.g., `thunderstorm.svg`, `clear.svg`, etc.).

- **`updateWeatherInfo()`**:
  - This function updates the weather details (temperature, humidity, wind speed, weather condition) on the page.

- **`updateForecastsInfo()`**:
  - This function fetches and displays the 7-day weather forecast. It filters the forecast data to display only the future dates (excluding the current day).

- **`showDisplaySection()`**:
  - This function controls the visibility of sections based on the state (e.g., showing the weather info or a "not found" message if the city is invalid).

---

## API

This app uses the **OpenWeatherMap API** to fetch weather data. To make the app work, you need an API key from OpenWeatherMap.

- **API Key**: You can get your free API key [here](https://openweathermap.org/appid).
- **API Endpoints**:
  - **Current weather**: `/weather?q={city}&appid={API_KEY}&units=metric`
  - **Future forecast**: `/forecast?q={city}&appid={API_KEY}&units=metric`

The app uses the `weather` and `forecast` endpoints to display current weather and 4-day forecasts.

---

## Folder Structure

```
/weather-web-app
├── index.html        # The main HTML file
├── style.css         # The CSS file for styling
├── script.js         # JavaScript file containing logic for the app
├── assets/           # Folder containing images and weather icons
│   ├── bg.jpg        # Background image for the app
│   └── weather/      # Weather icons (e.g., thunderstorm.svg, clear.svg)
|   └── message/      # Preview picture for search and city not found
└── README.md         # This file
```

---

## Acknowledgements

- **OpenWeatherMap API**: For providing the weather data.
- 
---

### Notes:

- You can customize the **API key** in the `script.js` file.
- The app currently uses **metric units** (°C for temperature, m/s for wind speed).

Let me know if you need any adjustments or additional information in the README!
