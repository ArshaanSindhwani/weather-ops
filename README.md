# Weather DataOps Pipeline

## Overview

Weather DataOps Pipeline is a JavaScript-based DataOps project that demonstrates automated data ingestion, processing, testing, containerisation, and deployment through a weather monitoring pipeline.

The application retrieves live weather data from the OpenWeather API, stores the latest weather information in JSON format, appends historical records to a CSV log, and visualises trends through an interactive web dashboard. A GitHub Actions workflow automates data collection and deployment, showcasing core DataOps and CI/CD principles.

This project was developed during La Fosse Academy to explore data pipeline automation, API integration, testing, Docker containerisation, and continuous delivery.

---

## Technologies

### Backend

- JavaScript (Node.js)
- Express.js

### Data Processing

- OpenWeather API
- JSON
- CSV

### Testing

- Jest

### Visualisation

- Plotly.js

### DevOps & Deployment

- Docker
- GitHub Actions
- CI/CD Pipelines
- Render

---

## Key Features

- Automated weather data ingestion from OpenWeather API
- Stores latest weather data in JSON format
- Maintains historical weather records in CSV format
- REST API endpoints for current and historical weather data
- Interactive weather dashboard
- Plotly temperature trend visualisation
- Automated testing with Jest
- Docker containerisation
- GitHub Actions CI/CD workflow
- Automated deployment through Render

---

## Architecture

```text
OpenWeather API
        │
        ▼
fetchWeather.js
        │
        ├── weather.json
        └── weather_log.csv
                    │
                    ▼
              Express API
                    │
       ┌────────────┴────────────┐
       ▼                         ▼
 /api/weather          /api/weather-log
       │                         │
       └────────────┬────────────┘
                    ▼
             Frontend Dashboard
                    │
                    ▼
               Plotly Charts
```

## My Contribution

I worked on implementing and integrating the core DataOps pipeline, including:

- API integration with OpenWeather
- Automated data collection and transformation
- JSON and CSV data storage
- Express API development
- Frontend dashboard integration
- Plotly chart visualisation
- Docker containerisation
- Automated testing using Jest
- GitHub Actions CI/CD workflow implementation
- Deployment pipeline configuration

---

## Screenshots

### Dashboard Overview

![Dashboard Overview](screenshots/dashboard-overview.png)

### Temperature Trend Visualisation

![Temperature Chart](screenshots/temperature-chart.png)

### Current Weather API Endpoint

![Weather API Endpoint](screenshots/api-weather-endpoint.png)

### Historical Weather Log Endpoint

![Weather Log Endpoint](screenshots/api-weather-log.png)

---

## CI/CD Pipeline

The project uses GitHub Actions to automate the complete data pipeline:

1. Install dependencies
2. Retrieve latest weather data
3. Update JSON and CSV datasets
4. Execute automated tests
5. Commit updated weather files
6. Trigger deployment to Render

This demonstrates a practical implementation of DataOps principles by automating data collection, validation, version control, and deployment.

---

## Testing

Automated tests validate:

- Weather JSON file structure
- CSV log integrity
- Data availability
- Data consistency between pipeline runs

Run tests locally:

```bash
npm test
```

## Running Locally

### Install Dependencies

```bash
npm install
```

### Configure Environment Variables

Create a `.env` file:

```env
WEATHER_API_KEY=your_api_key
CITY=London
```

### Fetch Weather Data

```bash
node fetchWeather.js
```

### Start the Application

```bash
node app.js
```

Visit:

```text
http://localhost:5000
```

---

## Docker

Build the container:

```bash
docker build -t weather-dataops .
```

Run the container:

```bash
docker run -p 5000:5000 weather-dataops
```

---

## What I Learned

Through this project I gained practical experience with:

- DataOps principles and workflows
- API integration and data ingestion
- Data transformation and storage
- Automated testing
- CI/CD pipelines
- GitHub Actions
- Docker containerisation
- Data visualisation
- Environment variable management
- Automated deployment workflows

---

## Future Improvements

- Add support for multiple cities
- Store historical data in a database
- Implement weather forecasting features
- Add alerting for extreme weather conditions
- Introduce data quality monitoring
- Add dashboard filtering and analytics
- Deploy using Kubernetes for scalability

---

## Repository Structure

```text
WeatherDataOps/
├── .github/workflows/
├── data/
│   ├── weather.json
│   └── weather_log.csv
├── public/
│   ├── client.js
│   ├── index.html
│   └── style.css
├── screenshots/
│   ├── dashboard-overview.png
│   ├── temperature-chart.png
│   ├── api-weather-endpoint.png
│   └── api-weather-log.png
├── tests/
│   └── weather.spec.js
├── app.js
├── fetchWeather.js
├── Dockerfile
├── package.json
└── README.md
```
