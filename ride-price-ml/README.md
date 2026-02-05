# Ride Price Estimation – Machine Learning Project

## Project Overview
This project builds a **machine learning regression model** to estimate the **price of a ride** based on trip details and surrounding conditions such as distance, time, traffic, and weather.  
The aim is to simulate how real ride-hailing services predict fares instead of using fixed rules.
---

## Dataset Description
- The dataset is **synthetically created** by the student.
- It contains **160 ride records**.
- Each row represents one ride scenario.
- The dataset includes both **numerical** and **categorical** features.
- The target variable is **`ride_price`**, which is a continuous value.

The data was designed with logical patterns, for example:
- Longer distance → higher price  
- Night rides → slightly higher fare  
- Rain or heavy traffic → increased cost  

---

## Features Used & Justification

### Main Features
| Feature | Type | Why It Matters |
|--------|------|----------------|
| `distance_km` | Numerical | Longer trips usually cost more. |
| `duration_min` | Numerical | Time spent on the ride affects price. |
| `time_of_day` | Categorical | Night or peak hours may have surcharges. |
| `traffic_level` | Categorical | Heavy traffic increases travel time and fuel use. |
| `weather` | Categorical | Bad weather often raises demand and price. |

### Additional Features Added
| Feature | Type | Reason for Adding |
|--------|------|------------------|
| `demand_level` | Categorical | Represents surge pricing situations when many people request rides at the same time. This helps the model learn price changes beyond just distance and time. |
| `day_type` | Categorical | Distinguishes **Weekday vs Weekend**. Weekends usually have higher demand, making the dataset more realistic. |

These two extra features were added to include **market behavior and demand effects**, not only physical trip details.

---

## Target Variable
| Variable | Description |
|---------|------------|
| `ride_price` | The estimated cost of the ride (continuous value). |

---

## Machine Learning Approach
- **Model Used:** Linear Regression  
- **Reason:** The target variable is continuous, so regression is suitable for predicting exact prices rather than categories.

---

## How to Run
1. Open the notebook in **Google Colab** or Jupyter Notebook.
2. Make sure the dataset path points to `data/rides.csv`.
3. Run all cells from top to bottom.

---

## Key Steps Performed
- Data loading and exploration  
- Handling missing values and inconsistencies  
- Encoding categorical features  
- Scaling numerical features  
- Training a Linear Regression model  
- Evaluating predictions using error metrics  
- Plotting predicted vs actual prices  

---

## Key Findings
- **Distance** and **demand level** were the most influential features.
- Traffic and weather also affected predictions.
- Adding weekend and demand features improved realism.

---

## Limitations
- The dataset is synthetic and may not perfectly match real-world data.
- Some real pricing factors (driver availability, location zones, etc.) are not included.
- Linear regression may not capture very complex pricing patterns.

---

## Conclusion
This project demonstrates how machine learning can be used to estimate ride prices using structured data.  
By designing a realistic dataset and applying a clear ML workflow, the model can learn meaningful relationships between trip conditions and ride cost.
