# 🐈 FelineCast

### Predictive Urban Colony Analytics & Targeted TNR Logistics

**IBM Z Datathon 2026 | Team Aristocats**  
**Track:** Wildcard – Beyond the Obvious  
**Platform:** IBM LinuxONE Community Cloud (s390x)

## Overview

FelineCast is a data-driven forecasting and resource allocation project designed to support proactive management of free-roaming cat populations.

Using historical animal shelter records, statistical modeling, and geographic visualizations, FelineCast predicts stray cat intake trends and identifies high-risk areas where Trap-Neuter-Return (TNR) interventions may be most effective.

Our goal is to help animal shelters, local governments, and community organizations make more informed decisions about population management and resource allocation.

## The Problem

Free-roaming cat overpopulation presents challenges for animal welfare, urban biodiversity, and municipal shelter systems.

Traditional animal control approaches are often reactive, responding to increasing shelter intakes rather than anticipating population growth.

FelineCast explores how predictive analytics can help communities identify emerging hotspots and prioritize sterilization efforts before seasonal population surges.

## Our Approach

Our initial implementation focuses on **Long Beach, California**, analyzing historical shelter data across 11 ZIP codes.

The project follows four main steps:

1. **Data Collection:** Combine Long Beach Animal Care Services (LBACS) records from 2017–2026 with U.S. Census household data.
2. **Data Processing:** Filter and organize more than 27,000 records to focus on stray cat intakes and TNR-related activities.
3. **Statistical Modeling:** Apply negative binomial regression to account for overdispersion in monthly intake counts.
4. **Forecasting & Visualization:** Generate ZIP-code-level forecasts and geographic visualizations to identify potential intervention hotspots.

### Why Negative Binomial Regression?

Monthly shelter intake counts exhibit overdispersion, where the variance exceeds the mean.

Negative binomial regression is better suited to this type of count data than standard Poisson regression. It also provides an interpretable approach for modeling population trends using relatively limited ZIP-code-level time-series data.

## Key Features

- **Population Forecasting:** Generate monthly stray cat intake forecasts for the next 12 months.
- **Geographic Hotspot Detection:** Visualize historical and projected intake patterns across Long Beach ZIP codes.
- **TNR Resource Planning:** Translate forecasts into estimated trap deployment and clinic voucher requirements.
- **Risk Assessment:** Compare intake trends with baseline colony estimates to identify priority intervention areas.
- **Interactive Visualizations:** Explore forecast maps, charts, and geographic trends.

## TNR Resource Allocation

FelineCast translates forecast results into illustrative resource allocation estimates:

- **Traps to Deploy:** Forecast × 1.5
- **Clinic Vouchers:** Estimated Traps × 0.8

For example, ZIP code **90805 (North Long Beach)** was identified as a priority hotspot in our demonstration, with a forecast of approximately 50 monthly intakes for October 2026.

These estimates demonstrate how forecasting can support targeted field operations and resource planning.

## Technology Stack

- **Platform:** IBM LinuxONE Community Cloud (s390x)
- **Programming Language:** Python
- **Development Environment:** JupyterLab
- **Statistical Modeling:** Negative Binomial Regression
- **Data Sources:** Long Beach Animal Care Services and U.S. Census
- **Data Formats:** CSV, GeoJSON
- **Outputs:** Forecast charts, geographic maps, and animated visualizations

The model was developed and trained within the IBM LinuxONE JupyterLab environment.

## Repository Structure

```text
FelineCast/
├── cat-alog.ipynb
├── clean.ipynb
├── negative_bi-meow-mial_model.ipynb
├── cat_forecast_map.ipynb
├── forecast_outputs/
├── forecast_next_12_months_long.csv
├── long_beach_california_cats_with_tnr_all_years.csv
├── long_beach_FILTERED_ONLY.csv
├── long_beach_zctas.geojson
├── long_beach_zip_boundaries.geojson
├── long_beach_cat_forecast.html
├── intake_map.gif
├── outlook_all_zips.png
└── README.md
```

## Impact & Future Potential

FelineCast aims to shift community cat management from reactive sheltering toward proactive, data-driven intervention.

Potential benefits include:

- **Animal Welfare:** Supporting targeted sterilization efforts to reduce unmanaged population growth.
- **Resource Efficiency:** Helping municipalities prioritize limited traps, clinic appointments, and field resources.
- **Wildlife Conservation:** Supporting efforts to reduce ecological pressures associated with unmanaged cat populations.
- **Scalability:** Extending the forecasting framework to other cities with standardized animal shelter datasets.

Future development could incorporate additional municipalities, environmental variables, and more advanced resource allocation strategies.

## Team Aristocats

- Selin Yilmaz
- Jacob Salmon
- Yihan Wang
- Dylan Ferrer
- Kevin Bernichio
- Luna Ferrer

**Developed for the IBM Z Datathon 2026.**
