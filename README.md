# Seattle vs. Atlanta: Which city rain more intesely vs more frequently (2018 - 2022)

## Project Overview:
This project analyzes and compares precipitation patterns between Seattle and Atlanta, challenging common precipitations nuance of rainfall pattern in these cities.  Using five years of daily precipitation data from a single station, we uncovered distinct rainfall characterisitics that provide practical insights for residents and visitor, general audience who plans to visit these cities.

## Data
Data Sourced from the National Centers for Environment Information (NCEI):
  - Seattle: GHCND:US1WAKG0225 (Seattle 2.1 ESE, WA) at 47.6117°N, 122.3085°W
  - Atlanta: Weather station at Hartsfield-Jackson International Airport
  - Time Period: Jan 1st, 2018 - Dec 31st, 2022
  - [NCEI Data Access](https://www.ncei.noaa.gov/cdo-web/search?datasetid=GHCND)

## Analysis
Our workflow summary:
1. **Data Preparation**
  - Standardized datatime (object -> DateTime)
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
Duy Nguyen
