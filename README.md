# US Home Price Factors Data Analysis

## DATA COLLECTION: [https://fred.stlouisfed.org/].

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

## DATA CLEANING: DataCleaning.ipynb
The data cleaning function does the following:

1. **Function**: `process_and_save_csv` loads, formats, resamples (if needed), filters by date range, renames columns, and saves the cleaned CSV to "CleanData".
2. **Directory**: Ensures "CleanData" directory exists.
3. **Processing**: Iterates through a list of datasets, applying the function to each for standardized cleaning and saving.

