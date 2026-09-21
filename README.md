# Asynchronous-Weather-Flight-Tracker-Dashboard

## 🌍 City & Air Traffic Real-Time Dashboard

A sleek, responsive web dashboard that provides real-time local weather, air quality metrics (US AQI), active regional flight tracking, and an interactive radar map for any city worldwide.

![License](https://img.shields.io/badge/license-MIT-blue.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)
![Leaflet](https://img.shields.io/badge/Leaflet-199900?style=flat&logo=leaflet&logoColor=white)

---

## ✨ Features

- 🔍 **Global City Search:** Converts city names into geographic coordinates using the Open-Meteo Geocoding API.
- 🌡️ **Real-Time Weather Metrics:** Live updates on temperature, relative humidity, precipitation, and wind speed.
- 🍃 **Air Quality Status:** Displays US AQI levels accompanied by color-coded safety badges (*Good*, *Moderate*, *Unhealthy*).
- ✈️ **Live Air Traffic Tracking:** Displays active flights in a ~100 km radius around the selected city with callsigns, altitude, speed, and heading (via OpenSky Network with an automatic fallback generator for API resilience).
- 🗺️ **Interactive Radar Map:** Renders live position markers for the target city and nearby aircraft using Leaflet.js and OpenStreetMap.
- 🌙 **Dark / Light Theme Switcher:** Fully adaptive theme support with persistent preference saved in `localStorage`.
- ⚡ **Performance & Polling Optimizations:**
  - In-memory client-side caching with a 3-minute TTL to reduce redundant network calls.
  - Automatic background polling every 30 seconds that bypasses cache for up-to-date live tracking.

---

## 🛠️ Tech Stack & APIs

* **Frontend:** HTML5, CSS3 (CSS Custom Properties & CSS Grid), Vanilla JavaScript (ES6+ / Async-Await).
* **Mapping Library:** [Leaflet.js](https://leafletjs.com/) with [OpenStreetMap](https://www.openstreetmap.org/) tiles.
* **External APIs Used:**
  * [Open-Meteo Geocoding API](https://open-meteo.com/en/docs/geocoding-api) – Geocoding location queries.
  * [Open-Meteo Weather Forecast API](https://open-meteo.com/) – Live weather data.
  * [Open-Meteo Air Quality API](https://open-meteo.com/en/docs/air-quality-api) – Real-time AQI metrics.
  * [OpenSky Network API](https://opensky-network.org/) – Regional flight state vectors.

---

## 📁 Project Structure

```text
├── index.html          # HTML structure and Leaflet CDN bindings
├── style.css           # Modern, responsive layout with CSS variables
├── script.js          # API calls, cache layer, map updates, and theme handler
```

🚀 Getting Started
No server-side installation or build steps are required. You can run the dashboard directly in any browser.

##1. Clone the repository
git clone [https://github.com/your-username/city-air-traffic-dashboard.git](https://github.com/your-username/city-air-traffic-dashboard.git)
cd city-air-traffic-dashboard

##2. Launch the Application
Simply open index.html in your web browser of choice, or use a local dev server like VS Code's Live Server extension:
```Bash
# Using Python to start a quick local server
python -m http.server 8000
```
Then navigate to http://localhost:8000 in your browser.

💻 Usage
1. Type any city name into the Search Location input field.

2. Click Fetch Live Data (or press Enter).

3. View current weather conditions, air quality levels, and nearby air traffic in real-time.

4. Interact with the map by panning or clicking on flight markers to view altitude and callsign details.

5. Use the theme button in the top-right corner to toggle between Light and Dark mode.

📄 License
This project is open-source and available under the MIT License.
