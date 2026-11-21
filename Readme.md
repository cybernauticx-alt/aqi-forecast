# AQI Forecast — Live Air Quality Trends & 12-Hour Prediction

A lightweight, single-file web dashboard for tracking live Air Quality Index (AQI) levels, pollutant breakdowns, daily and weekly trends, and 12-hour multi-factor AQI predictions for **Gurgaon**, **Delhi NCR**, and any city worldwide.

Live site: [aqiforecast.online](https://www.google.com/search?q=https://aqiforecast.online/)

## Features

* **Multi-Location Support:** Switch between Gurgaon, New Delhi, Noida, Faridabad, Ghaziabad, Chandigarh, Jaipur, Mumbai, Bengaluru, or search any custom city via the [Open-Meteo Geocoding API](https://open-meteo.com/en/docs/geocoding-api).
* **12-Hour Multi-Factor AQI Forecast:** Predicts the next 12 hours of US AQI using an in-browser ridge-regularized regression model trained on logged readings, incorporating temperature, wind speed & direction, humidity, rainfall washout, rush-hour patterns, CO, NO₂, and diurnal cycles from the [Open-Meteo Air Quality](https://open-meteo.com/en/docs/air-quality-api) and [Weather](https://open-meteo.com/en/docs) APIs.
* **What-If Weather Simulator:** Test how wind speed, temperature shifts, and rainfall impact the 12-hour AQI curve.
* **Daily & Weekly Trends:** View day-by-day breakdowns, 24-hour time-of-day patterns, and Sunday–Saturday weekly comparisons.
* **Deep Analytics:** Includes model fit metrics (`R²`, `MAE`, `RMSE`), `PM2.5 / PM10` combustion-vs-dust ratio tracking, an hourly spike/anomaly detector, and a full Pearson correlation matrix.
* **Actionable Guidance & Alerts:** Displays the cleanest 2-hour outdoor window, indoor air purifier/mask/ventilation recommendations based on [US EPA AQI](https://www.airnow.gov/aqi/aqi-basics/) tiers, custom high/clean AQI browser alerts, and one-tap **Share Summary** formatting.
* **Auto-Refresh & Mobile Ready:** Refreshes automatically every 10 minutes (or on every page load and city switch), with dark/light mode and home-screen web-app support.

## Tech Stack

* Single self-contained `index.html` (no build step or backend required)
* [Tailwind CSS](https://tailwindcss.com/) (Play CDN)
* [Chart.js](https://www.chartjs.org/)
* [Open-Meteo APIs](https://open-meteo.com/en/docs) (keyless, free for non-commercial use)

## Deployment on GitHub Pages

1. Rename `gurgaon-aqi-forecast-dashboard.html` to `index.html` and upload it alongside this `README.md` to a public [GitHub](https://github.com/) repository.
2. Open **Settings → Pages** in your repository, choose the `main` branch and `/ (root)` folder, and click **Save** ([GitHub Pages Quickstart](https://docs.github.com/en/pages/quickstart)).
3. To connect a custom domain (`aqiforecast.online`), add it under **Settings → Pages → Custom domain**, point your DNS `A` records (`@`) to [GitHub Pages' official IP addresses](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site) (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`) and `www` `CNAME` to `<your-username>.github.io`, and enable **Enforce HTTPS**.
