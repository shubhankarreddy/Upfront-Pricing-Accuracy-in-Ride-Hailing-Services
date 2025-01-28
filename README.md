# Upfront-Pricing-Accuracy-in-Ride-Hailing-Services
Analyzing factors affecting ride-hailing price deviations to improve upfront pricing accuracy and enhance customer satisfaction.


## Project Overview

Ride-hailing services like Uber and Ola use upfront pricing to estimate ride costs before booking. While convenient, deviations between the estimated upfront price and the actual metered price can lead to customer dissatisfaction. This project analyzes the factors contributing to such deviations and proposes methods to improve prediction accuracy.

## Problem Statement

Ride-hailing apps calculate upfront prices based on predicted ride distance and duration. If the actual price deviates by more than 20% from the upfront estimate, the metered price is charged instead. This project aims to identify the causes of price deviations and suggest ways to enhance pricing accuracy, reducing surprises for customers.

## Dataset Description

The dataset contains variables crucial for understanding price deviations:

- **order\_id\_new**: Unique identifier for each ride.
- **metered\_price**: Actual ride price.
- **upfront\_price**: Estimated price shown before booking.
- **predicted\_distance/duration**: Estimated distance and time for the ride.
- **gps\_confidence**: Indicator of GPS accuracy (1 = good, 0 = poor).
- **fraud\_score**: Rider's likelihood of fraudulent activity.
- **dest\_change\_number**: Number of times the destination was altered during the ride.
- **change\_reason\_pricing**: Reason for price adjustment (e.g., destination change).

## Key Findings

- **Price Deviations**: 39.89% of rides deviated by more than 20% from the upfront price.
- **GPS Accuracy**: 10.91% of rides had low GPS confidence, impacting prediction reliability.
- **Time Trends**: Price deviations and ride durations varied significantly by time blocks.

## Methodology

1. **Data Cleaning and Preprocessing**:
   - Removed unnecessary variables like app versions and device identifiers.
   - Handled missing values and outliers.
2. **Exploratory Data Analysis**:
   - Identified correlations between variables like GPS confidence and price deviations.
   - Analyzed patterns in ride duration, distance, and time of day.
3. **Visualization**:
   - Created Power BI dashboards to showcase insights on price deviations, GPS accuracy, and time trends.
4. **Modeling**:
   - Developed regression models to predict metered prices using Python (optional enhancement).

## Results

- Clear patterns were observed in price deviations based on time of day and GPS accuracy.
- The insights can help ride-hailing companies refine their pricing algorithms and improve customer satisfaction.

## Challenges and Limitations

- **Data Quality**: Some rides lacked reliable GPS data.
- **Destination Changes**: Frequent alterations in destinations complicated price predictions.
- **Modeling Assumptions**: Simplified models may not capture all real-world complexities.

## Future Work

- Implement machine learning models to predict metered prices in real-time.
- Analyze the impact of external factors like traffic and weather on pricing.
- Integrate customer feedback to assess satisfaction with price accuracy.

## Tools and Technologies Used

- **Python**: Data preprocessing and modeling.
- **Power BI**: Dashboard creation and visualization.
- **Pandas and NumPy**: Data manipulation.
- **Matplotlib and Seaborn**: Exploratory visualizations.

## How to Replicate the Analysis

1. Clone this repository.
2. Download the dataset and place it in the `data/` folder.
3. Run the Python scripts in the `scripts/` folder for data preprocessing and analysis.
4. Open the Power BI dashboard in the `results/` folder for visualization insights.

## Project Structure

```
ride-hailing-pricing-analysis/
|
|-- data/
|   |-- processed_ride_hailing_data.csv
|
|-- scripts/
|   |-- data_cleaning.py
|   |-- exploratory_analysis.py
|
|-- results/
|   |-- PowerBI_Dashboard.pbix
|   |-- visualizations/
|
|-- README.md
```


