# Titanic Dataset Exploratory Data Analysis (EDA)

This project conducts an in-depth exploratory data analysis (EDA) of the Titanic dataset, aiming to uncover the factors that contributed to the survival or demise of passengers. Through visualizations and statistical analysis, we investigate how different features such as age, class, gender, and more influenced survival rates.

## Project Structure

### Data Loading and Merging
- The notebook loads the `train.csv` dataset and combines it with the `test.csv` and `gender_submission.csv` datasets to create a more comprehensive dataset for analysis.

### Data Cleaning
- Irrelevant columns like Ticket and Cabin are dropped.
- Rows with missing values are removed to ensure a clean dataset.

### Feature Analysis
- Each feature in the dataset is analyzed to understand its distribution and its impact on survival.

### Visualizations
- Various plots are created to visualize the data, including histograms, bar plots, scatter plots, and Kernel Density Estimation (KDE) plots.

## Requirements

- **Python 3.x**
- **Libraries:**
  - pandas
  - matplotlib
  - seaborn
  - missingno

You can install the required libraries using pip:

```bash
pip install pandas matplotlib seaborn missingno
```

## Feature Analysis and Insights

1. **Survival (Target Variable)**
   - **Visualization:** A bar plot is used to visualize the number of passengers who survived (Survived = 1) versus those who did not (Survived = 0).
   - **Insights:**
     - The majority of passengers did not survive the disaster. The ratio of survivors to non-survivors is a crucial metric as it sets the baseline for analyzing other features.
     - This feature serves as the target variable for predicting survival.

2. **Pclass (Passenger Class)**
   - **Visualization:** KDE plots are used to compare the age distributions across different classes.
   - **Insights:**
     - **Distribution:** Passengers in 1st class tend to be older, while those in 3rd class are younger.
     - **Impact on Survival:** Passengers in 1st class had a higher chance of survival compared to those in 3rd class. This can be attributed to better access to lifeboats and priority during the evacuation.

3. **Age**
   - **Visualization:**
     - A histogram shows the age distribution of passengers.
     - A scatter plot of survival by age reveals how age impacted survival.
   - **Insights:**
     - **Distribution:** The age distribution is right-skewed, with most passengers being between 20 and 40 years old.
     - **Impact on Survival:** The scatter plot indicates that younger passengers, particularly children, had a higher survival rate, likely due to the "women and children first" policy during the evacuation.

4. **Sex**
   - **Visualization:** (Not explicitly present in the current notebook, but crucial for analysis)
     - Typically, a bar plot or pie chart can be used to visualize the survival rates based on gender.
   - **Insights:**
     - **Impact on Survival:** Female passengers had a significantly higher survival rate compared to male passengers. This was largely due to societal norms at the time, where women and children were prioritized during rescue operations.

5. **SibSp (Number of Siblings/Spouses aboard)**
   - **Visualization:** (Could be added for deeper analysis)
     - A bar plot could show survival rates based on the number of siblings/spouses aboard.
   - **Insights:**
     - **Impact on Survival:** Passengers with 1-2 siblings or spouses had a slightly better survival rate. Those traveling alone or with many family members had a lower chance of survival, possibly due to the chaos during the evacuation.

6. **Parch (Number of Parents/Children aboard)**
   - **Visualization:** (Could be added for deeper analysis)
     - Similar to SibSp, a bar plot could illustrate survival based on the number of parents/children aboard.
   - **Insights:**
     - **Impact on Survival:** Passengers traveling with 1-3 children or parents had a higher chance of survival, likely due to the prioritization of families during the evacuation.

7. **Fare**
   - **Visualization:** (Could be enhanced with KDE or box plots)
     - A distribution plot (histogram or KDE) could show the fare distribution among different passenger classes.
   - **Insights:**
     - **Impact on Survival:** Higher fares were often associated with 1st class tickets, which in turn correlated with higher survival rates. The fare can be seen as a proxy for social status, which influenced survival.

8. **Embarked (Port of Embarkation)**
   - **Visualization:** (Could be visualized with bar plots)
     - A bar plot could show survival rates based on the port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton).
   - **Insights:**
     - **Impact on Survival:** Passengers who embarked from Cherbourg (C) had higher survival rates, potentially due to a higher proportion of 1st class passengers boarding there.

9. **Missing Data**
   - **Visualization:** The `missingno.matrix` visualization helps in identifying missing data.
   - **Insights:**
     - **Handling Missing Data:** Missing data is primarily in the Age, Cabin, and Embarked features. For robust analysis, Cabin and Ticket were dropped, while rows with missing values in other features were removed.

## Insights Summary

- **Key Features:**
  - Pclass, Age, and Sex were the most significant features influencing survival, with clear patterns showing higher survival rates among 1st class passengers, younger individuals, and females.
- **Feature Relevance:**
  - Features like Pclass and Sex directly correlated with social status and access to lifeboats, making them critical predictors of survival.
  - Age provided insights into the priority given to younger passengers during the evacuation.
  - Fare served as an indirect measure of socio-economic status, influencing survival.

## Conclusion

The EDA provides a comprehensive view of the factors influencing survival on the Titanic. By examining features like passenger class, age, and sex, we gain valuable insights into the social dynamics and decision-making during the disaster. This analysis lays the groundwork for more sophisticated predictive models.
