# Exploratory Data Analysis: Cars Dataset 2025
 
 This project is a deep dive into a kaggle dataset containing over 1,200 car models. The goal was to clean the data, explore market trends, and use statistics to understand what actually drives car performance and pricing.

## Project Overview

- Which brands offer the most variety?
- Does more horsepower always mean faster acceleration?
- How does seating capacity relate to a car's "performance" status?

## Key Findings

- Standard Seating: 5-seater vehicles are the most common configuration in the market
- Brand Leaders: Nissan leads in model diversity, while Porsche maintains the strongest performance positioning.
- Performance: High horsepower (>300 hp) is statistically proven to result in faster acceleration (p < 0.0001).
- Price Drivers: Engine capacity (CC), Horsepower, and Torque are the primary factors that determine a car's price.
- The "Sports" Segment: Cars that hit 0-100 km/h in under 6 seconds are almost always 2 or 4-seaters.
- Torque and Horsepower showed the strongest positive correlation with Price, meaning they are the primary "value drivers" in the 2025 car market.

## Data Cleaning Steps

To make this analysis accurate, I performed several cleaning steps:

- Standardization: Fixed column names for better readability (e.g., converted "CC/Battery Capacity" to "Battery_Capacity(cc)").
- Numeric Conversion: Used Regex to extract numbers from strings like "$1,100,000" or "340 km/h" so they could be used for math.
- Special Cases: Cleaned the "Seats" column to handle unique values like "2+2" (converted to 4) and fixed encoding errors (like ï¿½).
- Missing Values: Analyzed and handled null values in performance and capacity columns.

## Visualizations Included

- Brand Distributions: Which companies have the most models in the dataset.
- Correlation Heatmaps: Relationships between Price, Horsepower, and Speed.
- Performance Analysis: Bar charts and histograms showing how seating affects acceleration.

## Statistical Analysis & Hypothesis Testing

To ensure the insights were accurate and not just due to random chance, I performed several statistical operations:

1. Hypothesis Testing (Two-Sample T-Test)
I tested the relationship between Horsepower and Acceleration (0-100 km/h).
The Goal: To see if high-horsepower cars (>300 hp) actually accelerate faster than lower-horsepower cars.
The Result: The test returned a p-value < 0.0001.
Conclusion: Since the p-value is much lower than 0.05, we can statistically confirm that higher horsepower significantly improves acceleration speeds.

2. Chi-Square Test of Independence
I used this test to see if a car's Seating Capacity is related to its Performance Category (Sports vs. Regular).
The Goal: To determine if certain seating layouts (like 2-seaters) are mathematically more likely to be classified as "Performance" cars.
The Result: A significant relationship was found, proving that seating configuration is a strong predictor of a car's performance segment.

3. Correlation Matrix
I calculated the correlation coefficients between all numeric variables (Price, CC, HP, Torque, Top Speed). 

## Technologies Used

- Python
- Pandas (Data manipulation)
- Matplotlib & Seaborn (Data visualization)
- Scipy (Statistical hypothesis testing)

## Key Files
- `Cars_EDA.ipynb`: Main analysis notebook
- `Cars_Datasets_cleaned.csv`: Processed dataset
