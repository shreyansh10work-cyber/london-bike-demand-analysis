# 🚲 London Bike Sharing Demand Analysis

## 📌 Project Overview

This project analyses **London bike-sharing demand** using Python to identify how bicycle usage changes across different times, days, seasons, weather conditions, holidays, temperature levels and humidity.

The objective of the project is not only to visualise historical bike-sharing data, but also to generate **business insights that could help improve fleet allocation, bike redistribution, staffing, maintenance planning and demand forecasting**.

---

## 🎯 Business Problem

Bike-sharing demand is not constant throughout the day.

The number of bicycles required can change significantly depending on:

* Time of day
* Day of the week
* Weekday vs weekend
* Public holidays
* Season
* Weather conditions
* Temperature
* Humidity
* Wind speed

For a bike-sharing operator, poor demand planning may result in:

* Stations having no bikes available
* Stations becoming completely full
* Poor customer experience
* Inefficient bike redistribution
* Higher operating costs
* Poor utilisation of bicycles

This project explores historical London bike-sharing data to understand these demand patterns and identify opportunities for better operational decision-making.

---

# 📂 Dataset

The dataset used in this project was obtained from **Kaggle**.

**Source:** Kaggle – London Bike Sharing Dataset

The dataset contains approximately **17,414 hourly observations** related to London bike-sharing activity.

The analysis is conducted for educational and portfolio purposes.

> Dataset credit belongs to the original dataset creator and Kaggle publisher.

---

## 📊 Dataset Variables

| Variable       | Description                            |
| -------------- | -------------------------------------- |
| `timestamp`    | Date and time of the observation       |
| `cnt`          | Number of bike rentals                 |
| `t1`           | Actual temperature                     |
| `t2`           | Feels-like temperature                 |
| `hum`          | Humidity                               |
| `wind_speed`   | Wind speed                             |
| `weather_code` | Weather condition code                 |
| `is_holiday`   | Indicates whether the day is a holiday |
| `is_weekend`   | Indicates whether the day is a weekend |
| `season`       | Season code                            |

Additional variables were created during data preparation, including:

* Year
* Month
* Month name
* Day
* Day name
* Hour
* Date
* Season name
* Weather name

---

# 🛠️ Technologies Used

The project was completed using:

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Jupyter Notebook

---

# 🧹 Data Cleaning and Preparation

Before conducting the analysis, the dataset was inspected and cleaned.

The following steps were performed:

1. Loaded the dataset using Pandas.
2. Checked the number of rows and columns.
3. Inspected data types.
4. Checked for missing values.
5. Checked for duplicate observations.
6. Removed duplicate records where required.
7. Converted `timestamp` into datetime format.
8. Created time-based variables such as hour, day, month and year.
9. Converted coded variables into readable categories.
10. Created readable weather and season labels.
11. Prepared the cleaned dataset for exploratory data analysis.

The original dataset contained:

* **17,414 observations**
* **10 original variables**
* **No missing values**
* **No duplicate rows**

---

# 🔍 Exploratory Data Analysis

The project investigates several important areas of bike-sharing demand.

The main analyses include:

* Bike demand by hour
* Bike demand by day of week
* Weekday vs weekend demand
* Hour × day heatmap
* Monthly bike-sharing trends
* Seasonal demand
* Weather impact
* Temperature vs bike demand
* Humidity vs bike demand
* Holiday vs normal-day demand
* Correlation analysis

---

# 📈 Key Business Insights

## 1. Strong Morning and Evening Commuter Peaks

The analysis shows a strong relationship between bike demand and commuting hours.

The highest average demand occurs at approximately:

### 08:00 AM

Average demand:

**≈ 2,883 bike rentals per hour**

Another major demand peak occurs during the evening.

Approximate demand:

| Time  | Average Rentals |
| ----- | --------------: |
| 08:00 |           2,883 |
| 17:00 |           2,830 |
| 18:00 |           2,629 |

This indicates that London bike-sharing usage is strongly influenced by **commuting behaviour**.

### 💡 Business Recommendation

Bike redistribution should take place **before the morning and evening commuting peaks**.

Operators should ensure high-demand stations contain sufficient bikes before approximately:

* 07:00–08:00
* 16:00–17:00

Maintenance or station closures should be avoided during these periods where possible.

---

# 2. Weekdays Have Higher Demand Than Weekends

Average hourly bike demand is approximately:

| Day Type | Average Rentals |
| -------- | --------------: |
| Weekday  |           1,209 |
| Weekend  |             977 |

Weekday demand is approximately **24% higher than weekend demand**.

This further supports the importance of commuting behaviour in bike-sharing usage.

### 💡 Business Recommendation

More bikes and redistribution resources should be available during weekdays.

Weekend operations can focus more heavily on recreational and midday travel patterns rather than traditional commuter peaks.

---

# 3. Midweek Bike Demand Is Strong

The analysis indicates that **Thursday has the highest average bike demand**.

Average Thursday demand is approximately:

**1,259 rentals per hour**

Tuesday and Wednesday also demonstrate strong usage.

Sunday records the lowest average demand at approximately:

**960 rentals per hour**

### 💡 Business Recommendation

Operational resources should be prioritised during the middle of the working week, particularly:

* Tuesday
* Wednesday
* Thursday

---

# 4. Season Has a Major Impact on Demand

Bike-sharing usage changes considerably across seasons.

Approximate average hourly demand:

| Season | Average Rentals |
| ------ | --------------: |
| Summer |           1,464 |
| Autumn |           1,179 |
| Spring |           1,104 |
| Winter |             822 |

Summer bike demand is approximately **78% higher than winter demand**.

### 💡 Business Recommendation

Fleet availability should be increased during warmer months.

Winter could provide opportunities for additional:

* Bicycle maintenance
* Dock maintenance
* Fleet servicing
* Infrastructure improvements
* Staff training

because overall demand is considerably lower.

---

# 5. Weather Strongly Influences Bike Demand

Weather conditions have a significant relationship with bike-sharing usage.

Approximate average demand observed in the dataset:

| Weather Condition | Average Rentals |
| ----------------- | --------------: |
| Few Clouds        |           1,496 |
| Broken Clouds     |           1,195 |
| Clear             |           1,162 |
| Rain              |             713 |
| Cloudy            |             635 |
| Rain + Thunder    |             583 |
| Snowfall          |             251 |

Poor weather conditions are associated with substantially lower bike usage.

Snowfall produces particularly low bike demand.

### 💡 Business Recommendation

Weather forecasts could be incorporated into daily operational planning.

For example:

**Good weather forecast**

⬇

Higher expected demand

⬇

More bikes available at high-demand stations

Whereas:

**Poor weather forecast**

⬇

Lower expected demand

⬇

Reduced redistribution requirements

---

# 6. Temperature Has a Positive Relationship With Bike Demand

The analysis found an approximate correlation of:

**r = +0.389**

between actual temperature and bike demand.

This represents a moderate positive relationship.

In general:

**Higher Temperature → Higher Bike Demand**

### 💡 Business Recommendation

Temperature forecasts could be used as one input in a future bike-demand prediction model.

---

# 7. Humidity Has a Negative Relationship With Demand

Humidity demonstrates an approximate correlation of:

**r = -0.463**

with bike demand.

This suggests:

**Higher Humidity → Lower Bike Demand**

Interestingly, humidity has a stronger relationship with bike demand than temperature within this dataset.

### 💡 Business Recommendation

Demand forecasting should consider humidity together with temperature and weather conditions rather than relying on temperature alone.

---

# 8. Holidays Have Lower Bike Demand

Average demand is approximately:

| Day Type   | Average Rentals |
| ---------- | --------------: |
| Normal Day |           1,152 |
| Holiday    |             770 |

Bike demand on holidays is approximately **33% lower** than on normal days.

This is likely connected to reduced commuting activity.

### 💡 Business Recommendation

Operators may require fewer commuting-focused redistribution activities during public holidays.

Maintenance and operational activities could potentially be scheduled during lower-demand holiday periods.

---

# 🧠 Overall Business Insight

The analysis demonstrates that London bike-sharing demand is mainly influenced by two groups of factors.

## Time-Based Factors

* Hour of day
* Day of week
* Weekend status
* Holiday status
* Season

## Environmental Factors

* Temperature
* Humidity
* Weather
* Wind speed

The strongest pattern visible in the analysis is the relationship between bike demand and **weekday commuting behaviour**.

Weather and seasonal conditions further influence the level of demand.

---

# 💼 Business Recommendations

Based on the analysis, a bike-sharing operator could implement the following strategies:

### 🚲 Fleet Redistribution

Redistribute bicycles before major commuter demand periods, particularly before:

* 08:00
* 17:00–18:00

---

### ☀️ Weather-Based Demand Planning

Use weather forecasts to anticipate daily demand.

Good weather should trigger preparations for higher demand, while severe weather may indicate lower demand.

---

### 📅 Weekday Resource Planning

Allocate more bikes and operational staff during weekdays compared with weekends.

---

### 🌞 Seasonal Fleet Planning

Increase operational bicycle availability during summer.

Use lower-demand winter periods for additional maintenance.

---

### 🔧 Maintenance Scheduling

Schedule maintenance during periods with historically lower demand, such as:

* Late-night hours
* Sundays
* Holidays
* Winter periods
* Severe weather periods

---

### 📊 Predictive Demand Management

Historical demand patterns could be combined with weather forecasts to predict future bike-sharing demand.

This would allow the operator to move from **reactive bike redistribution to proactive bike redistribution**.

---

# 💰 Potential Business Impact

Applying these insights could potentially help a bike-sharing operator:

* Reduce the number of empty stations
* Reduce completely full stations
* Improve bike availability
* Improve customer experience
* Increase bicycle utilisation
* Reduce unnecessary redistribution
* Improve workforce planning
* Improve maintenance scheduling
* Improve seasonal resource allocation
* Reduce operating costs
* Support data-driven decision-making

---

# 🤖 Next Stage: Predictive Analytics

The next phase of this project can extend the exploratory analysis into machine learning.

The target variable would be:

```python
cnt
```

which represents bike demand.

Potential predictor variables include:

```text
Hour
Day of Week
Month
Weekend
Holiday
Season
Temperature
Feels-like Temperature
Humidity
Wind Speed
Weather Condition
```

Possible models include:

### 1. Linear Regression

Used as a simple baseline model.

### 2. Random Forest Regression

Used to identify nonlinear patterns and important demand drivers.

### 3. Gradient Boosting Regression

Used to potentially improve prediction accuracy.

---

# 📏 Model Evaluation

Prediction models can be compared using:

### MAE

Mean Absolute Error

Shows the average difference between predicted and actual bike demand.

### RMSE

Root Mean Squared Error

Provides greater penalties for large prediction errors.

### R² Score

Measures how much variation in bike demand is explained by the model.

---

# 🔎 Future Analysis

Future improvements to the project could include:

* Machine learning demand prediction
* Feature importance analysis
* Hour × weather interaction analysis
* Weekday × hour analysis
* Seasonal forecasting
* Time-series forecasting
* Power BI dashboard
* Tableau dashboard
* Interactive demand dashboard
* Real-time weather integration

---

# 📁 Project Structure

```text
London-Bike-Sharing-Analysis/
│
├── LondonTFL.ipynb
│
├── london_merged.csv
│
├── london_bike_cleaned.csv
│
├── README.md
│
└── images/
    ├── hourly_demand.png
    ├── weekday_weekend.png
    ├── demand_heatmap.png
    ├── seasonal_demand.png
    ├── weather_demand.png
    └── correlation_heatmap.png
```

---

# ▶️ How to Run the Project

## 1. Clone the Repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

## 2. Navigate to the Project Folder

```bash
cd London-Bike-Sharing-Analysis
```

## 3. Install Required Libraries

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

## 4. Open Jupyter Notebook

```bash
jupyter notebook LondonTFL.ipynb
```

Run each notebook cell sequentially.

---

# 📚 Dataset Source

The dataset used in this project was obtained from:

**Kaggle – London Bike Sharing Dataset**

Platform:

**Kaggle**

The dataset is used for educational, analytical and portfolio purposes.

All credit for the original dataset belongs to the respective dataset creator and publisher on Kaggle.

> The exact Kaggle dataset URL can be added here if required.

---

# 🎯 Project Outcome

The project demonstrates how Python can be used to transform raw transportation data into useful business insights.

The analysis identified clear:

* Commuter demand patterns
* Seasonal demand differences
* Weather-related behaviour
* Weekday/weekend differences
* Holiday effects
* Temperature relationships
* Humidity relationships

The findings could support better bike redistribution, fleet availability, staffing, maintenance and future demand forecasting.

---

# 👤 Author

**Shreyansh Chaudhary**


---

## ⭐ If you found this project useful

Feel free to explore the notebook, review the analysis and connect with me on GitHub or LinkedIn.
