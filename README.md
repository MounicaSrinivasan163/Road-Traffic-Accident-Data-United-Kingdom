# 🚧 Road Accidents Dataset Analysis

## 📌 Summary
This dataset contains detailed records of road traffic accidents reported in the UK. It provides information about accident severity, date/time, location, road types, weather, vehicle involvement, lighting conditions, and more. It is ideal for exploring patterns in accident severity, geographic risk, and environmental effects.

---
##🔍 Key Highlights
- Over 300,000 records of accidents, 21 columns

- Covers location, time, weather, road types, casualties, and more

- Enables temporal, geospatial, and environmental analysis

- High potential for machine learning tasks (classification, risk modeling)


## 🧩 Dataset Structure

| Column                       | Description                                               | Type         |
|-----------------------------|-----------------------------------------------------------|--------------|
| Accident_Index              | Unique ID of the accident                                 | Categorical  |
| Accident Date               | Date on which the accident occurred                       | Categorical  |
| Day_of_Week                 | Day of the week                                           | Categorical  |
| Junction_Control            | Type of traffic control at the junction                   | Categorical  |
| Junction_Detail             | Description of junction (e.g. Crossroads, T-junction)     | Categorical  |
| Accident_Severity           | Severity level (e.g. Serious, Slight, Fatal)              | Categorical  |
| Latitude                    | GPS coordinate                                            | Continuous   |
| Longitude                   | GPS coordinate                                            | Continuous   |
| Light_Conditions            | Light conditions at time of accident                     | Categorical  |
| Local_Authority_(District)  | District of local authority                               | Categorical  |
| Carriageway_Hazards         | Road hazards present (e.g. oil, object, animal)           | Categorical  |
| Number_of_Casualties        | Number of injured/killed individuals                      | Continuous   |
| Number_of_Vehicles          | Number of vehicles involved                               | Continuous   |
| Police_Force                | Police force that reported the accident                   | Categorical  |
| Road_Surface_Conditions     | Road surface status (wet, dry, etc.)                      | Categorical  |
| Road_Type                   | Type of road (Single carriageway, One-way, etc.)          | Categorical  |
| Speed_limit                 | Speed limit at the accident site (in mph)                 | Continuous   |
| Time                        | Time of day of the accident                               | Categorical  |
| Urban_or_Rural_Area         | Context of the area (Urban/Rural)                         | Categorical  |
| Weather_Conditions          | Weather at time of accident                               | Categorical  |
| Vehicle_Type                | Type of vehicle involved (e.g., Car, Taxi)                | Categorical  |

---

## ✅ Use Cases

- 🕒 Time Series Analysis: Find peak accident times.
- 🗺️ Geospatial Risk Mapping: Spot accident-prone areas.
- 🌦️ Weather Impact Study: Analyze severity based on weather.
- 🛣️ Road Type Risk Profiling: Understand which road types are riskier.
- 🚔 Authority Performance: Evaluate districts with the most severe accidents.
- 🏙️ Urban vs Rural: Compare safety between regions.

---

## ❓ Medium-Level Pandas Questions

1. What is the distribution of accidents over the days of the week?
2. Which weather condition is most associated with serious accidents?
3. Compare accident severity between urban and rural areas.
4. What is the average number of casualties per accident for each road type?
5. How does accident severity vary with speed limits?
6. Find the top 10 most accident-prone districts.
7. Analyze how time of day (morning, afternoon, evening, night) affects severity.
8. Count accidents per month and identify the peak accident month.
9. What is the proportion of accidents with poor lighting conditions?
10. Group by vehicle type and calculate the mean number of casualties.

---

## 🧠 Complex-Level Pandas Challenges

1. **Multivariate Pivot Table**  
   Create a pivot table with `Weather_Conditions` and `Road_Surface_Conditions` as rows, `Accident_Severity` as columns, and counts as values.

2. **Geographic Filtering + Aggregation**  
   Filter accidents within a bounding box (e.g. London area), then find the average `Number_of_Casualties` by `Road_Type`.

3. **Severity Prediction Feature Engineering**  
   Add a binary column `is_high_speed` (Speed_limit > 50), and analyze severity distribution across it.

4. **Time-of-Day Binning**  
   Bin accident `Time` into categories (Morning, Afternoon, Evening, Night) and compare severity across bins.

5. **Missing Value Handling & Imputation**  
   Identify columns with missing values, impute `Carriageway_Hazards` with `'None'`, and handle missing `Time` appropriately.


