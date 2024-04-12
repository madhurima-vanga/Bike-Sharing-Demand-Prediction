**Bike Sharing Demand Prediction**

**Context**
Currently Rental bikes are introduced in many urban cities for the enhancement of mobility comfort. It is important to make the rental bike available and accessible to the public at the right time as it lessens the waiting time. Eventually, providing the city with a stable supply of rental bikes becomes a major concern. The crucial part is the prediction of bike count required at each hour for the stable supply of rental bikes.
The dataset contains weather information (Temperature, Humidity, Windspeed, Visibility, Dewpoint, Solar radiation, Snowfall, Rainfall), the number of bikes rented per hour and date information.

**Objective**
This notebook is a thorough resource describing the goals, procedures, and results of our data mining project, which aims to increase the precision of demand projections for Seoul's bike sharing program. Our method delivers reliable predictions by methodically gathering and creating pertinent data elements, as well as by using several regression models. After a thorough review, the model that was adopted gives interpretability top priority in order to shed light on the variables affecting the demand for bikes. For stakeholders and data enthusiasts interested in improving urban mobility and sustainable transportation options, the notebook provides insightful analysis and recommendations.

**Data Dictionary**
* Date : year-month-day
* Rented Bike count - Count of bikes rented at each hour
* Hour - Hour of the day
* Temperature-Temperature in Celsius
* Humidity - %
* Windspeed - m/s
* Visibility - 10m
* Dew point temperature - Celsius
* Solar radiation - MJ/m2
* Rainfall - mm
* Snowfall - cm
* Seasons - Winter, Spring, Summer, Autumn
* Holiday - Holiday/No holiday
* Functional Day - NoFunc(Non Functional Hours), Fun(Functional hours)

**Approach**

* Objective: paragraph explaining what this notebook provides, why, & approach
* Import Libraries & Data Overview (include data dictionary)
* Exploratory Data Analysis
* Data Preparation
* Data Partitioning
* Model Building
* Performance Evaluation
* Model Comparison & Selection

**Feature scaling**: 
* Scaling is a preprocessing technique in machine learning that transforms the numerical values of features to a standardized range, ensuring equal contribution to model training.

* Min-Max scaling normalizes data to a specific range, typically [0, 1], by subtracting the minimum and dividing by the range.

* Standard scaling, or Z-score normalization, centers data with a mean of 0 and a standard deviation of 1, achieved by subtracting the mean and dividing by the standard deviation.

* Both methods enhance model performance by preventing features with larger scales from dominating others during the learning process.

**Models:**
1. Linear Regression
2. Ridge Regression
3. Random Forest
4. Xgboot

**Performance metrics of Regression Model**:
* **MSE (Mean Squared Error)**: A measure of the average squared difference between predicted and actual values. It penalizes larger errors more heavily, making it sensitive to outliers.

* **MAE (Mean Absolute Error)**: The average absolute difference between predicted and actual values. It provides a more straightforward representation of the average error without squaring the differences.

* **RMSE (Root Mean Squared Error)**: The square root of the MSE, providing a measure of the average magnitude of the errors. It is in the same units as the dependent variable, making it easier to interpret than MSE.

* **R-squared (R^2)**: A statistical measure indicating the proportion of the variance in the dependent variable that is predictable from the independent variables. It ranges from 0 to 1, with 1 indicating a perfect fit. It's a measure of how well the model explains the variability in the data.

**Conclusion:**

* Among the models evaluated, XGB Regression stands out as the most promising choice for the dataset dataset. It exhibits the **lowest Mean Squared Error (MSE)** at **28,438.48** and **the highest R-squared value of 0.9299**, indicating a strong predictive performance.

* Additionally, its Root Mean Squared Error (RMSE) of 168.64 and Mean Absolute Error (MAE) of 100.56 are competitive, signifying accurate predictions and minimal deviation from the actual values.

* The XGB Regression model outperforms Linear Regression and Ridge Regression, demonstrating its ability to capture complex relationships within the data. Considering its robust performance metrics, the XGB Regression model appears to be the most suitable choice for your predictive modeling task.
