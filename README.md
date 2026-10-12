# Weather Intelligence

A weather dashboard that pulls live data from Open-Meteo and predicts temperatures with a linear regression trained in your browser. Built around Alpharetta, GA, with other cities you can search.

**Live site:** https://sahasreddye-sys.github.io/weather-prediction-model/

![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-notebook-3776AB?logo=python&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-blue)
![GitHub Pages](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-222?logo=github)

## What it does

- Current conditions and forecast from Open-Meteo (free, no API key).
- Tabs for Today, Forecast, Analytics, Model, Accuracy and Cities.
- Search any city, or use your location.
- Trains a linear regression on about two years of that city's history each time you load it, then shows how its predictions compare to what happened.

## How well it works

The model predicts tomorrow's mean temperature. On the Alpharetta data when I checked on October 11, 2026, it was trained on 724 days and scored a mean absolute error of about 2.3°F with R² of about 0.64 on a held-out test set. These numbers are recomputed every time the page loads, so they move a little day to day. The Accuracy tab compares past predictions to what actually happened.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole dashboard. Plain HTML, CSS and JavaScript, no dependencies. |
| `Weather_Analysis_Model.ipynb` | Notebook for Alpharetta: data pull, feature engineering and a comparison of six models. Linear regression did best, which is why the site uses it. |

## Run it locally

```bash
git clone https://github.com/sahasreddye-sys/weather-prediction-model.git
cd weather-prediction-model
python -m http.server 8000
```

Open http://localhost:8000. It needs an internet connection for the Open-Meteo requests. The page can take a few seconds to fill in while the history downloads and the model trains.

## Limits

- The model only uses past weather for the city, not pressure maps or radar, so it is a baseline and not a replacement for a real forecast.
- Accuracy varies by city and season. The Accuracy tab shows the current numbers.

## License

MIT, see `LICENSE`.
# Weather Intelligence

A weather dashboard that pulls live data from Open-Meteo and predicts temperatures with a linear regression trained in your browser. Built around Alpharetta, GA, with other cities you can search.

**Live site:** https://sahasreddye-sys.github.io/weather-prediction-model/

![JavaScript](https://img.shields.io/badge/JavaScript-vanilla-F7DF1E?logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-notebook-3776AB?logo=python&logoColor=white)
![GitHub Pages](https://img.shields.io/badge/hosted%20on-GitHub%20Pages-222?logo=github)

## What it does

- Current conditions and forecast from Open-Meteo (free, no API key).
- Tabs for Today, Forecast, Analytics, Model, Accuracy and Cities.
- Search any city, or use your location.
- Trains a linear regression on about two years of that city's history each time you load it, then shows how its predictions compare to what happened.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole dashboard. Plain HTML, CSS and JavaScript, no dependencies. |
| `Weather_Analysis_Model.ipynb` | Notebook for Alpharetta: data pull, feature engineering and a comparison of six models. Linear regression did best, which is why the site uses it. |

## Run it locally

```bash
git clone https://github.com/sahasreddye-sys/weather-prediction-model.git
cd weather-prediction-model
python -m http.server 8000
```

Open http://localhost:8000. It needs an internet connection for the Open-Meteo requests.

## Limits

- The model only uses past weather for the city, not pressure maps or radar, so it is a baseline and not a replacement for a real forecast.
- Accuracy varies by city and season. The Accuracy tab shows the current numbers.
