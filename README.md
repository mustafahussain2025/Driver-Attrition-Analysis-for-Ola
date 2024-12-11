## Driver Attrition Analysis for Ola

## Problem Statement

Recruiting and retaining drivers is a significant challenge for Ola due to high churn rates. Drivers can easily switch to competitors like Uber based on fluctuating rates, creating instability. This issue negatively impacts organizational morale and increases costs, as acquiring new drivers is more expensive than retaining existing ones. Moreover, losing drivers frequently disrupts operations.

The objective of this analysis is to predict whether a driver will leave the company based on their demographic and performance attributes. This predictive insight will allow Ola to implement proactive strategies to improve retention rates, thereby reducing costs and improving operational stability.

Key driver attributes analyzed include:
- Age, gender, and education level
- Monthly income
- City of operation
- Employment tenure and joining designation
- Business value generated
- Quarterly performance ratings

## Approach

### 1. Exploratory Data Analysis (EDA)
- **Data Structure:** Examined dataset structure, including rows, columns, and data types.
- **Missing Value Analysis:** Identified columns with missing data and prepared for imputation.
- **Descriptive Statistics:** Summarized numerical attributes to understand distribution, trends, and outliers.
- **Temporal Analysis:** Analyzed monthly join and leave rates and calculated the average driver tenure.
- **Visualization:** Plotted distributions of key features like age, income, and total business value.

### 2. Data Preprocessing
- **Imputation:** Handled missing values using mean, median, or mode for numerical columns, and domain knowledge for categorical attributes.
- **Target Variable Creation:** Derived a target variable indicating whether a driver has left based on the `LastWorkingDate` column.
- **Feature Engineering:**
  - Calculated the age of drivers at the time of joining.
  - Flagged whether a driver’s quarterly rating and income have increased over time.
  - Encoded categorical variables like city and education level using one-hot encoding.
- **Class Imbalance Treatment:** Balanced the dataset using oversampling techniques like SMOTE.
- **Standardization:** Scaled numerical features to normalize values.

### 3. Predictive Analysis
- Built and evaluated machine learning models to predict attrition. Techniques included:
  - Logistic Regression for interpretability.
  - Random Forest and Gradient Boosting for higher accuracy.
- Assessed models using metrics like accuracy, precision, recall, and F1-score.

### 4. Insights and Recommendations
- Identified factors strongly correlated with attrition, such as:
  - Low quarterly ratings
  - Declining monthly income
  - Short tenure or late career joining
- Recommended targeted interventions:
  - Incentivize high-performing drivers through bonuses or promotions.
  - Improve income stability by reducing variability in earnings.
  - Implement tenure-based rewards to encourage long-term commitment.

### Tools Used
- Python: For data analysis and modeling.
- Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn.
- Jupyter Notebook: For documenting and presenting the analysis.

## Conclusion

This project highlights the importance of understanding driver behavior and leveraging predictive analytics to address high attrition rates. The analysis provides actionable insights that Ola can implement to reduce churn and improve driver retention. By focusing on identified key factors and utilizing predictive models, Ola can foster a more stable and cost-effective workforce, strengthening its competitive position in the ride-hailing industry.


