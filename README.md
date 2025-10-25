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
```

Weather-Prediction-Application/
│
├─ index.html        # Main HTML page
├─ style.css         # Stylesheet for UI
├─ script.js         # JavaScript to fetch API and render data
└─ assets/           # Images, icons, backgrounds

````

---

## Installation & Setup
1. Clone the repository:
```bash
git clone https://github.com/gowthamgspatil/Weather-Prediction-Application.git
cd Weather-Prediction-Application
````

2. Open `index.html` in a browser to run the application.
3. (Optional) If using a server:

   * Install dependencies
   * Create a `.env` file and add your weather API key:

     ```env
     WEATHER_API_KEY=your_api_key_here
     ```
   * Start the server:

     ```bash
     npm start
     ```

---

## Usage

1. Enter a city name in the search box.
2. Press "Search" or Enter.
3. View weather information including temperature, humidity, wind speed, and pressure.
4. Invalid inputs will trigger an alert message.

---

## Example Code Snippet

### Fetching Weather Data (JavaScript)

```javascript
const apiKey = "YOUR_API_KEY"; // Replace with your API key
const cityInput = document.getElementById("cityInput");
const searchBtn = document.getElementById("searchBtn");
const resultDiv = document.getElementById("result");

searchBtn.addEventListener("click", () => {
    const city = cityInput.value.trim();
    if(city === "") {
        alert("Please enter a city name");
        return;
    }

    fetch(`https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}&units=metric`)
        .then(response => response.json())
        .then(data => {
            if(data.cod === 200){
                resultDiv.innerHTML = `
                    <h2>${data.name}, ${data.sys.country}</h2>
                    <p>Temperature: ${data.main.temp} °C</p>
                    <p>Min: ${data.main.temp_min} °C, Max: ${data.main.temp_max} °C</p>
                    <p>Humidity: ${data.main.humidity}%</p>
                    <p>Wind Speed: ${data.wind.speed} m/s</p>
                `;
            } else {
                alert("City not found. Please try again.");
            }
        })
        .catch(err => alert("Error fetching weather data"));
});
```

---

## Future Enhancements

* 5-day / 7-day forecast
* Geolocation detection for automatic city
* Celsius/Fahrenheit unit toggle
* Dark mode
* Historical weather data visualization
* Multi-language support
* More dynamic UI/UX effects based on weather

---

## Contributing

1. Fork the repository
2. Create a feature branch:

```bash
git checkout -b feature/YourFeature
```

3. Commit your changes:

```bash
git commit -m "Add YourFeature"
```

4. Push to branch:

```bash
git push origin feature/YourFeature
```

5. Submit a Pull Request

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## Contact

* Author: **Gowtham G. S. Patil**
* GitHub: [gowthamgspatil](https://github.com/gowthamgspatil)

