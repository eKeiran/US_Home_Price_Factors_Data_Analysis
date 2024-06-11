# US Home Price Factors Data Analysis

**GOAL:** To find available data for key factors that influence US home prices nationally. Then, build a data science model that explains how these factors impacted home prices over the last 20 years. 

*Final Result Summary:* Training and evaluating Ridge Regression, Random Forest Regression, and Gradient Boosting Regression models. 
### <u>Out of three models chosen, <em>Random Forest</em> most accurately explains how key factors impacted home prices with the highest R Square Score and lowest Mean Absolute Error.</u>

![image](https://github.com/eKeiran/US_Home_Price_Factors_Data_Analysis/assets/34791715/a04df742-c540-4975-a284-2c04d8d326d2)

<p align="center">
  <img src="https://github.com/eKeiran/US_Home_Price_Factors_Data_Analysis/assets/34791715/2028256c-bf76-4da2-b0a7-07a6781df401" alt="Second Image">
</p>

## I. DATA COLLECTION: [https://fred.stlouisfed.org/].

- CASE-SCHILLER Home Price Index - https://fred.stlouisfed.org/series/CSUSHPISA
- Consumer price index (CPI) - https://fred.stlouisfed.org/series/CPIAUCSL
- Construction price index - https://fred.stlouisfed.org/series/WPUSI012011
- Employment rate - https://fred.stlouisfed.org/series/LREM64TTUSM156S
- Housing Subsidies (Federal) - https://fred.stlouisfed.org/series/L312051A027NBEA
- Interest rates - https://fred.stlouisfed.org/series/FEDFUNDS
- Per Capita GDP - https://fred.stlouisfed.org/series/A939RX0Q048SBEA
- Percent urban population - https://data.worldbank.org/indicator/SP.URB.TOTL.IN.ZS?end=2021&locations=US&start=2001
- Real Median Household Income - https://fred.stlouisfed.org/series/MEHOINUSA672N
- Total households - https://fred.stlouisfed.org/series/TTLHH
- Unemployment rate - https://fred.stlouisfed.org/series/UNRATE
- Working population - https://fred.stlouisfed.org/series/LFWA64TTUSM647S

## II. DATA CLEANING: DataCleaning.ipynb
The data cleaning function does the following:

1. **Function**: `process_and_save_csv` loads, formats, resamples (if needed), filters by date range, renames columns, and saves the cleaned CSV to "CleanData".
2. **Directory**: Ensures "CleanData" directory exists.
3. **Processing**: Iterates through a list of datasets, applying the function to each for standardized cleaning and saving.

## III. EXPLORATORY DATA ANALYSIS: EDA.ipynb
The Exploratory Data Analysis (EDA) involved:

1. **Data Visualization**: Using seaborn and matplotlib to create visualizations like histograms, scatter plots, and correlation heatmaps.
2. **Correlation Analysis**: Analyzing the correlation between different features and the target variable using correlation matrices and pair plots.

## IV. MODEL TRAINING: ModelTraining.ipynb
The model training process included:

1. Splitting the data into training and testing sets.
2. Feature selection using Recursive Feature Elimination (RFE) with different regression models.
3. Training and evaluating Ridge Regression, Random Forest Regression, and Gradient Boosting Regression models.
4. Calculating Mean Absolute Error (MAE) and R-squared (R2) for each model.

## V. FINAL RESULT:

The trained models yielded the following results:

### Ridge Regression:

Mean Absolute Error (MAE): 🟥 **13.859**

R-squared (R2): 🟧 **0.996**

### Random Forest Regression:

Mean Absolute Error (MAE): 🟩 **4.577**

R-squared (R2): 🟩 **0.999**

### Gradient Boosting Regression:

Mean Absolute Error (MAE): 🟧 **5.888**

R-squared (R2): 🟩 **0.999**


## The Random Forest Regression and Gradient Boosting Regression models performed better than Ridge Regression based on lower MSE values and perfect R2 scores, indicating a strong predictive ability of these models for US home prices.
