# Flight Delay Prediction Using Random Forest
## Project Description
This project leverages machine learning to predict flight delays using a dataset of historical flight records in the US between 2019 and 2023. The goal is to identify key factors contributing to delays and provide actionable insights for improving operational efficiency in the aviation industry. The model is built to prioritize the recall of delayed flights, addressing the significant economic and logistical impacts of delays.

## Dataset
- Source: [Kaggle Airline Delay Dataset](https://www.kaggle.com/datasets/patrickzel/flight-delay-and-cancellation-dataset-2019-2023)
- Description:
  - The dataset contains over 3 million entries representing flight operations in the U.S.
  - Includes features such as flight schedule, delays, taxi times, and distance traveled.
  - The analysis focuses on the top 5 most popular destinations, resulting in a filtered dataset of **~600,000 entries**.

## Methodology
1. **Data Cleaning**:
- Removed cancelled and diverted flights.
- Reformatted timestamps and validated taxi time calculations.
2. **Exploratory Data Analysis:**
- Analyzed trends in delays by airline, destination, and time of day.
- Calculated average taxi-in and taxi-out times for each airport.
3. **Feature Engineering:**
- Added features like departure hour (HourofDay) and average taxi times (AVG_TAXI_IN and AVG_TAXI_OUT).
4.** Modeling:**
- Built a **Random Forest classifier** to predict flight delays (delayed vs. on-time).
- Evaluated performance using metrics like accuracy, F1-score, and recall.

## Key Results
1. **Performance**:
- Accuracy: 90%
- Recall for delayed flights: 75%
- F1-score for delayed flights: 0.76
2. **Feature Importance**:
- Departure delay (DEP_DELAY) was the most important feature (91% importance).
- Time of day (HourofDay) and average taxi times also contributed modestly.
3. **Limitations**:
- Heavy reliance on departure delay, which limits pre-departure prediction capability.
- Absence of critical features like weather data and historical airline delay trends.
4. **Recommendations**:
- Incorporate external data sources, such as:
  - Weather conditions (e.g., precipitation, wind speed).
  - Historical delay trends for airlines and airports.
- Explore alternative models (e.g., Gradient Boosting) and hyperparameter tuning to improve recall for delayed flights.
- Develop a real-time delay prediction system for operational use.
