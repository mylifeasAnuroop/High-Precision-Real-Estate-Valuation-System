# Predictive Real Estate Analysis

## Author : Anuroop Arya 

This project aims to predict real estate prices in Bangalore based on various factors such as location, total square feet area, number of bathrooms, and bedrooms (BHK). The model is built using Python, leveraging machine learning techniques.

## Approach

1. **Data Load and Cleaning:**
   - The data is loaded from a CSV file containing Bangalore home prices.
   - Irrelevant features like `area_type`, `society`, `balcony`, and `availability` are removed.
   - NA values are handled by dropping rows with missing values in critical columns (`location`, `size`, `bath`).

2. **Feature Engineering:**
   - Added a new feature `bhk` based on the `size` column.
   - Converted the `total_sqft` column to a uniform numeric value.
   - Added `price_per_sqft` to analyze the price variation based on the square feet area.

3. **Outlier Removal:**
   - Outliers are removed based on:
     - Square feet per bedroom threshold.
     - Standard deviation and mean price per square feet.
     - Number of bathrooms exceeding the number of bedrooms by 2.

4. **Dimensionality Reduction:**
   - Reduced the number of unique locations by tagging locations with fewer data points as `other`.

5. **Model Building:**
   - Used `Linear Regression`, `Lasso Regression`, and `Decision Tree Regressor` models.
   - Employed K-Fold cross-validation and GridSearchCV to find the best model.

6. **Pipeline Creation:**
   - Created a pipeline using `StandardScaler` and `LinearRegression` for streamlined model deployment.

7. **HTML and CSS Deployment:**
   - Developed an HTML page with CSS styling using Flask.
   - Deployed the model on the local host.

## Technologies Used

- **Python Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn
- **Web Development:** HTML, CSS, Flask

## Methodology

- **Data Cleaning:** Handling missing values and removing irrelevant features.
- **Feature Engineering:** Creating new features and transforming existing ones.
- **Model Building:** Developing regression models to predict housing prices.
- **Deployment:** Hosting the model on a local server using Flask.

## Real-World Applications

- **Real Estate Investment:** Predicting property prices for investment decisions.
- **Housing Market Analysis:** Analyzing trends in property prices based on various factors.
- **Business Intelligence:** Providing insights into potential property development areas.

