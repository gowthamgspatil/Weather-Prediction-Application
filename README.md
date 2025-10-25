# Weather Prediction Application

A web application that predicts the weather for any city using a weather API and displays it in a clean, responsive interface.

---

## Overview
This application allows users to input a city or location and view current weather conditions including:
- Temperature
- Minimum and maximum temperature
- Humidity
- Wind speed
- Atmospheric pressure

It fetches data from a weather API (e.g., OpenWeatherMap) and presents it dynamically in the UI.

---

## Features
- Search weather by city or location
- Display current temperature, min/max temperature, humidity, wind speed, and pressure
- Alerts for invalid or unknown locations
- Dynamic UI with weather-based visuals
- Responsive design for desktop and mobile

---

## Technologies Used
- **Frontend:** HTML5, CSS3, JavaScript
- **API Integration:** External Weather API (OpenWeatherMap or similar)
- **Libraries:** Optional (jQuery, Font Awesome)
- **Hosting/Deployment:** Can run as static site or on simple web server

---

## How It Works
1. User enters a location in the search box.
2. JavaScript sends a request to the weather API.
3. The API returns current weather data for the location.
4. Data is displayed on the page.
5. Invalid locations trigger an alert prompting the user to try again.
6. Optional: Background or visuals change based on weather conditions.

---

## Project Structure

Weather-Prediction-Application/
│
├─ index.html # Main HTML page
├─ style.css # Stylesheet for UI
├─ script.js # JavaScript to fetch API and render data
└─ assets/ # Images, icons, backgrounds


---

## Installation & Setup
1. Clone the repository:
```bash
git clone https://github.com/gowthamgspatil/Weather-Prediction-Application.git
cd Weather-Prediction-Application
