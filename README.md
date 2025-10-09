# Seattle vs. Atlanta: Comparing Frequency and Intensity (2018 - 2022)

## Project Overview:
This project analyzes and compares precipitation patterns between Seattle and Atlanta, challenging common precipitations nuance of rainfall pattern in these cities.  Using five years of daily precipitation data from a single station, we uncovered distinct rainfall characteristics that provide practical insights for residents and visitor, general audience who plans to visit these cities.

## Data
Data Sourced from the National Centers for Environment Information (NCEI):
  - Seattle: GHCND:US1WAKG0225 (Seattle 2.1 ESE, WA) at 47.6117°N, 122.3085°W
  - Atlanta: Weather station at Hartsfield-Jackson International Airport
  - Time Period: Jan 1st, 2018 - Dec 31st, 2022
  - [NCEI Data Access](https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND)

The processed datasets used in this analysis are available in the data folder: [seattle_rain.csv](https://github.com/dcnguyen060899/weather/blob/main/data/seattle_rain.csv), [atlanta_ga_rain.csv](https://github.com/dcnguyen060899/weather/blob/main/data/atlanta_ga_rain.csv), and the merged dataset [clean_seattle_atlanta_rain.csv](https://github.com/dcnguyen060899/weather/blob/main/data/clean_seattle_atlanta_rain.csv).

## Requirements
This project requires the following Python packages:
  - pandas: Data Manipulation and analysis
  - numpy: Numerical computations
  - matplotlib: Basic plotting and customization
  - seaborn: Statistical visualization
  - scipy: Statistical testing
  - statsmodels: Advanced statistical modelling

Environment:
  - Python 3
  - Jupyter Notebook/Lab and Visual Studio Code

All dependencies are listed in [requirements.txt](https://github.com/dcnguyen060899/weather/blob/main/requirements.txt), run pip install -r requirements.txt to install lirabries.

## Analysis
The complete data preparation and cleaning process is documented in [data_cleaning.ipynb](https://github.com/dcnguyen060899/weather/blob/main/code/data_cleaning.ipynb), while the exploratory data analysis, visualizations, and statistical testing are detailed in [eda_modelling.ipynb](https://github.com/dcnguyen060899/weather/blob/main/code/eda_modelling.ipynb). Both notebooks are located in the code folder of this repository.

Our workflow summary:
1. **Data Preparation**
  - Standardized datatime (object -> datetime64[ns])
  - Handle missing values using historical monthly averages
  - Created a unified, cleaned dataset ready for Exploratory Data Analysis and Modelling
2. **Missing Data Strategy**
  - Identified 190 missing values for Seattle (22 from original Seattle data + 168 outer merge missing data)
  - Imputed values using mean precipitation for same calendar day across years
  - Validated completeness of final dataset
  
3. **Exploratory Data Analysis**
  - Examined average precipitation pattern across cities
  - Visualized time series trends (2018-2022)
  - Analyzed seasonal variations using monthly aggregations.
  - Created specialized visualization for rainy days ONLY
  - Investigated rainfall frequency distributions

Lastly, we will also conduct statistical significant test (t-test and z-test) to double check whether what we see if in barplot by seaborn is indeed statistical different mean and proportion.

## Results
The complete findings and conclusions from this analysis are documented in the final report: [Seattle vs Atlanta Weather Project Report (PDF)](https://github.com/dcnguyen060899/weather/blob/main/reports/Communicate%20the%20Results%20%7C%20Weather.pdf), located in the reports folder. This report provides a comprehensive yet accessible overview of the rainfall pattern differences between the two cities, written for a general audience.

## Main Findings:
1. Rainfal Pattern:
  - Seattle: more rainy days across majority of the month but lighter rainfall (like drizzle, not thunderstorm)
  - Atlanta: less frequent but more intense rainfall (like thunderstorm in the early summer)

2. Seasonal Variation
  - Seattle: highest rainfall in the winter, practically no rain in the summer
  - Atlanta: most intense rainfall in the early summer
  - June show similar pattern between cities

3. Practical Implication:
  - Seattle Visitors: pack light raincoat or poncho (if you go fishing or camping) year-round, except summer
  - Atlanta Visitors: prepare for occasional heavy thunderstors, especially in summer

## Study Limitation
- Only 5-year of data point (2018 - 2022)
- Single weather station per city
- Result might not represent entire metropolitan areas

## Author
**Duy Nguyen**  
MS in Data Science - Seattle University

Email: [dnguyen44@seattleu.edu](mailto:dnguyen44@seattleu.edu)  
LinkedIn: [https://www.linkedin.com/in/duwe-ng/](https://www.linkedin.com/in/duwe-ng/)

## License
This project is licensed under the MIT License - Copyright (c) 2025 Duy Nguyen



