# London-Bike-Rides-Analysis

## Project Overview

🌟 This project analyzes London bike rides between 2015 and 2017 to explore key patterns, seasonal trends, and environmental factors influencing bike usage.

---
## Data Source
The dataset was sourced from Kaggle, providing detailed records of London bike rides from 2015 to 2017.

### Key Features:
- **Timeframe:** January 2015 to January 2017.
- **Variables:**
  - Real temperature, wind speed, humidity.
  - Seasonal and holiday ride breakdowns.
  - Daily bike ride counts.

### Example Data:
Below is a snapshot of the dataset:

![Dataset Example](assets/bikes_head.png)

---

## Tools and Technologies Used
- **Python**: For cleaning, preprocessing, and analyzing the data.
- **Tableau**: To build interactive dashboards for visual analysis.
- **Jupyter Notebook**: To document and execute Python scripts for data analysis.
- **Git & GitHub**: For version control and sharing the project.

---

## Data Cleaning and Analysis

### Sample Code Snippet
Below is a snippet of the Python code used for data cleaning and preprocessing:

```python
import pandas as pd

data = pd.read_csv('london_bikes_final.csv')
data['real_temp'] = data['temp_real_C'].fillna(data['temp_real_C'].mean())
data['ride_count'] = data['count']
data['is_weekend'] = data['is_weekend'].astype(bool)
data_cleaned = data.dropna()
```

### Sample Output:

```text
Average temperature: 12.47°C
Average rides per hour: 1,143
Optimal temperature range: 10–22°C
```

## Key Visualizations

### Tableau Dashboard

Explore the interactive Tableau dashboard for detailed visualizations:
[London Bike Rides Dashboard](https://public.tableau.com/app/profile/kateryna.zahrebina/viz/LondonBikeRides_17377457774600/Dashboard1)

### Sample Visualizations

1. **Two-day Moving Average of Bike Rides:**

   ![Moving Average Visualization](assets/moving_average.png)

2. **Temperature vs. Wind Speed Heatmap:**

   ![Temperature vs Wind Speed](assets/temperature_vs_wind_speed.png)

## Insights

### Total and Average Rides:
- **Total bike rides recorded:** 19,905,972.
- **Average bike rides per hour:** 1,143.

### Weather and Environmental Conditions:
- **Average temperature:** 12.47°C.
- **Average wind speed:** 15.91 kph.
- **Average humidity:** 72.3%.

### Seasonal Trends:
- Bike rides were highest in summer (6,424,609 rides), followed by autumn (5,073,040), spring (4,850,236), and winter (3,558,087).

### Impact of Weekends and Holidays:
- **Non-holiday weekdays:** 14,752,718 rides.
- **Weekends:** 4,857,756 rides.
- **Holidays:** 295,498 rides (relatively low impact).

### Temperature Influence:
- **Optimal range:** 10–25°C, peaking especially around 12.5–22.4°C.
- Extremely low (< 5°C) or high (> 27°C) temperatures significantly reduce rides.

### Wind Speed Influence:
- **Optimal range:** 0–21 kph. Significant drop above 25 kph.
- Very high wind speeds (> 39 kph) see minimal bike rides regardless of temperature.



---
## Conclusions
    
- **Seasonal Impact**: Summer sees the highest bike usage, indicating favorable weather conditions and longer daylight hours
- **Temperature**: Optimal conditions for biking are between 10–22°C, aligning with mild and pleasant weather
- **Wind Speed**: Minimal impact at lower speeds, but significantly reduces bike usage above 25 kph
- **Holidays**: Low activity on holidays may indicate fewer people commuting for work

## Future Improvements

1. Enhance analysis by including other factors like time of day or public events.
2. Optimize visualizations for clearer insights.
3. Implement machine learning models to predict future bike usage.
---


