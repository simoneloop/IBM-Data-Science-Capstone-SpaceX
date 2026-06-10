# IBM Data Science Capstone — SpaceX Falcon 9 Landing Prediction

> Can we predict whether the Falcon 9 first stage will land successfully?
> SpaceX charges ~$62M per launch (vs $165M+ for competitors) thanks to booster reuse.
> Accurate landing predictions enable cost estimation and competitive bidding.

**IBM Data Science Professional Certificate — Capstone Project**

---

## Project Pipeline

```
SpaceX REST API + Wikipedia Scraping
        ↓
Data Wrangling  (cleaning, binary label creation)
        ↓
EDA with SQL    (exploratory queries on launch data)
        ↓
EDA Visualization  (matplotlib / seaborn / plotly)
        ↓
Geospatial Analysis  (Folium interactive maps)
        ↓
ML Model Training  (Logistic Regression, SVM, Decision Tree, k-NN)
        ↓
Interactive Dashboard  (Dash / Plotly)
```

## Notebooks

| # | Notebook | Description |
|---|----------|-------------|
| 1 | [Data Collection — API](jupyter-labs-spacex-data-collection-api.ipynb) | Fetches launch records from the SpaceX REST API |
| 2 | [Data Collection — Web Scraping](jupyter-labs-webscraping.ipynb) | Scrapes Wikipedia for historical Falcon 9 launch tables |
| 3 | [Data Wrangling](labs-jupyter-spacex-Data%20wrangling-v2.ipynb) | Cleans data, engineers the binary `landing_class` target |
| 4 | [EDA with SQL](EDA%20with%20SQL.ipynb) | SQL queries on Db2: site stats, payload ranges, outcome counts |
| 5 | [EDA Visualization](edadataviz.ipynb) | Feature distributions, payload vs. success, time-series trends |
| 6 | [Launch Site Map](lab_jupyter_launch_site_location_with_folium.ipynb) | Folium map of launch sites with success/failure markers |
| 7 | [ML Prediction](SpaceX_Machine%20Learning%20Prediction_Part_5.ipynb) | Train/compare classifiers; hyperparameter tuning via GridSearchCV |

## Interactive Dashboard

`app.py` — Dash/Plotly app:
- **Dropdown**: filter by individual launch site or all sites
- **Range slider**: filter by payload mass (0 – 10 000 kg)
- Pie chart: success rate per site
- Scatter plot: payload mass vs. outcome, coloured by booster version

```bash
pip install dash pandas plotly
python app.py
```

## Features

| Feature | Description |
|---------|-------------|
| Launch Site | CCAFS LC-40, VAFB SLC-4E, KSC LC-39A, … |
| Payload Mass | 0 – 10 000+ kg |
| Booster Version | F9 v1.0/v1.1/FT/B4/B5 |
| Orbit | LEO, GEO, ISS, Polar, … |
| Customer | NASA, SpaceX, Iridium, … |
| Launch Date | Time-series from 2010 onward |

## Tech Stack

Python · Pandas · NumPy · Scikit-learn · SQL (Db2) · BeautifulSoup · Folium · Plotly · Dash · Jupyter

## Results

Full analysis and findings are summarised in the presentation: [`winning space race.pdf`](winning%20space%20race.pdf)
