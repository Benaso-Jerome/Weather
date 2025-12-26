# Weather App

A modern, responsive weather application that displays current weather conditions and 5-day forecasts for any city using the OpenWeather API.

## Features

- 🌡️ **Current Weather Display**
  - Real-time temperature, humidity, and weather conditions
  - Beautiful weather icons using FontAwesome
  - City name and location information

- 📅 **5-Day Forecast**
  - Daily weather predictions
  - Temperature ranges (min/max)
  - Humidity information
  - Weather condition icons

- 🎨 **Modern UI/UX**
  - Glassmorphism design with backdrop blur effects
  - Smooth animations and transitions
  - Dark mode support
  - Fully responsive design (mobile-friendly)

- ⚡ **Performance**
  - Parallel API calls for faster loading
  - Efficient data processing
  - Loading states and error handling

## Technologies Used

- **HTML5** - Structure and semantic markup
- **CSS3** - Styling with modern features (backdrop-filter, animations)
- **JavaScript (ES6+)** - Async/await, fetch API, DOM manipulation
- **FontAwesome 6.4.0** - Weather icons
- **OpenWeather API** - Weather data source

## Setup Instructions

### 1. Get Your API Key

1. Visit [OpenWeatherMap](https://openweathermap.org/api)
2. Sign up for a free account
3. Navigate to the API keys section
4. Copy your API key

### 2. Configure API Key

Open `script.js` and replace the API key on line 19:

```javascript
const API_KEY = "YOUR_API_KEY_HERE";
```

Replace `YOUR_API_KEY_HERE` with your actual OpenWeather API key.

**Note:** The project currently includes a pre-configured API key. For production use, consider using environment variables or a secure configuration method.

### 3. Run the Application

Simply open `index.html` in your web browser. No build process or server required!

You can also use a local development server:

```bash
# Using Python 3
python -m http.server 8000

# Using Node.js (http-server)
npx http-server

# Using PHP
php -S localhost:8000
```

Then navigate to `http://localhost:8000` in your browser.

## How to Use

1. **Search for Weather**
   - Enter a city name in the search input field
   - Click the "Search" button or press Enter
   - Wait for the weather data to load

2. **View Current Weather**
   - See the current temperature, weather condition, and humidity
   - Large weather icon displays the current conditions

3. **Check 5-Day Forecast**
   - Scroll down to see the 5-day weather forecast
   - Each day shows temperature range, humidity, and weather icon

4. **Toggle Dark Mode**
   - Click the moon/sun icon in the top-right corner
   - Your preference is saved in localStorage

## File Structure

```
Weather/
│
├── index.html          # Main HTML structure
├── style.css           # All styling and animations
├── script.js           # JavaScript logic and API calls
└── README.md           # This file
```

## API Endpoints Used

The application uses the following OpenWeather API endpoints:

1. **Current Weather API**
   - Endpoint: `/data/2.5/weather`
   - Purpose: Get current weather conditions by city name
   - Parameters: `q` (city name), `units` (metric), `appid` (API key)

2. **5-Day Forecast API**
   - Endpoint: `/data/2.5/forecast`
   - Purpose: Get 5-day weather forecast by city name
   - Parameters: `q` (city name), `units` (metric), `appid` (API key)

## Code Structure

The JavaScript code is organized into clear sections:

- **Configuration** - API key and endpoint URLs
- **DOM Elements** - Element references
- **Initialization** - App setup and event listeners
- **API Functions** - Weather data fetching
- **DOM Manipulation** - Rendering weather data
- **Utility Functions** - Helper functions (icon mapping, formatting, etc.)

## Error Handling

The app includes comprehensive error handling for:

- Invalid API keys
- Network connection issues
- City not found errors
- Invalid input validation
- API rate limiting

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Features in Detail

### Input Validation
- Trims whitespace automatically
- Validates city name characters
- Shows appropriate error messages

### Loading States
- Disables input and button during API calls
- Shows loading spinner
- Prevents multiple simultaneous requests

### Theme Management
- Dark mode toggle
- Saves preference to localStorage
- Smooth theme transitions

### Responsive Design
- Mobile-first approach
- Adapts to different screen sizes
- Touch-friendly interface

## API Key Security Note

⚠️ **Important:** For production deployments, never commit your API key to version control. Consider:

- Using environment variables
- Implementing a backend proxy
- Using API key restrictions in OpenWeather dashboard
- Setting up CORS policies

## License

This project is open source and available for educational purposes.

## Credits

- Weather data provided by [OpenWeatherMap](https://openweathermap.org/)
- Icons by [FontAwesome](https://fontawesome.com/)

## Project Requirements Met

✅ Uses OpenWeather API  
✅ Displays current weather (temperature, humidity, icon)  
✅ Shows 5-day forecast  
✅ Day/night theme toggle  
✅ Real-world API usage with parameters and API keys  
✅ Data parsing and error handling  
✅ Clean code structure with 3 files (HTML, CSS, JS)

---

**Enjoy checking the weather!** ☀️🌧️❄️

