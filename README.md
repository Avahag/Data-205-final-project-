# Accident Rate and Contributing Factors
Overview
This project investigates the relationship between various traffic and environmental factors and accident rates in Montgomery County, Maryland. By analyzing accident data, traffic volumes, and infrastructure factors, the project aims to identify trends, patterns, and areas needing improvement to enhance road safety.

## Datasets
1. Montgomery County Crash Report Data
Contains 36 variables related to accidents.
Variables include vehicle year, make, and model, surface conditions, weather, time of day, accident location, and more.
2. MDOT SHA Annual Average Daily Traffic (AADT) Data
Contains traffic volume information used for calculations of Vehicle Miles Traveled (VMT).
## Objectives
Examine accident trends over time in Montgomery County (2015–2024).
Identify contributing factors such as weather conditions, vehicle types, surface conditions, and time of day.
Analyze accident patterns and visualize accident hotspots using choropleth and kernel density maps created in ArcGIS Pro.
Provide insights for infrastructure improvements and policy recommendations to reduce accidents.
Methodology
## Data Cleaning

Grouped variables (e.g., driver distractions, weather conditions) into more manageable categories for better analysis.
One-hot encoding for vehicle types (EV vs. non-EV).
## Analysis
Rolling Average Calculation: Applied a 3-year rolling average to smooth data fluctuations and capture longer-term trends.

Accident Rate Calculation:
The accident rate was calculated by dividing the total accident count for each year by the Vehicle Miles Traveled (VMT) for that year, multiplied by 100,000 to normalize the rate per million miles driven per vehicle.
VMT was calculated as the average annual traffic (AADT) for each year, multiplied by the corresponding road segment length.

Spearman’s Correlation:
Analyzed correlation between accident counts and continuous variables (e.g., speed limits).

Linear Regression:
Analyzed relationships between accident frequency and various factors (vehicle make, surface conditions, weather, etc.).

Multinomial Logistic Regression:
Investigated how vehicle type (EV vs non-EV) impacts injury severity.


Bivariate and Point Density Maps: 
Created bivariate maps and point density maps to analyze accident hotspots and their correlation with infrastructure projects and bike trail locations.

## Key Findings
Accident Trends:
The number of accidents remained stable from 2015–2019, with a sharp decline in 2020 due to the COVID-19 pandemic. Post-2020, accident counts started rising again but remained below pre-2020 levels.
Spearman’s Correlation:

A weak negative correlation (-0.115) between accident count and speed limit was found, but it was not statistically significant.
Impact of Vehicle Type:

Non-EVs are more likely to be involved in minor and non-injury accidents, with significant p-values for minor injuries and no injuries (e.g., p = 9.36e-08 for no injury).
Factors Affecting Accident Count:

Non-EVs were significantly associated with higher accident counts compared to EVs. Days of the week such as Wednesday and Thursday showed the highest likelihood of accidents.
Weather conditions, surface conditions (e.g., snow and ice), and lighting conditions also influenced accident patterns.
Bike Trails and Accident Distribution:

Maps showed that accidents tend to cluster in densely populated areas , particularly near bike trails, indicating potential safety concerns in these areas.

## Maps (ArcGIS pro)
Accident Locations and Infrastructure: Bivariate map visualizing the correlation between accidents and ongoing construction projects.
Bike Trail Accident Density: point density map showing accident distribution around bike trails.


## Conclusion
This project highlights the importance of comprehensive traffic data analysis for enhancing road safety. By considering various contributing factors, we can make data-driven recommendations for policy changes and infrastructure improvements to reduce accidents, particularly in high-risk areas.

## Running the Code
This project was implemented using R for statistical analysis and ArcGIS Pro for geospatial analysis.

# Dependencies:
R packages: dplyr, ggplot2, tidyverse, sf, lmtest, etc.
To run the project, ensure you have the required libraries and datasets, and execute the R scripts to analyze the data, followed by visualizing results through ArcGIS Pro.
