# The-analysis-of-bicycle-related-accidents-across-the-UK-from-1979-to-2018
---
## 1. Exploratory Data Analysis (EDA):
a. Dataset Overview:
This dataset contains detailed records of bicycle-related accidents across the UK from 1979 to 2018, totaling 827,861 rows and 14 columns. It includes:
- Environmental attributes (e.g., weather, road, light conditions)
- Temporal details (e.g., date, time, year, day of week)
- Casualty info: gender, age group, severity

b. Data Cleaning & Preparation:
- I merged both datasets using Accident_Index as the key.
- I removed unrealistic entries where the speed limit was above 130 mph.
- Then, dropped rows in which the weather, light, or road condition fields were absent.
- Next, I converted the Date column to datetime and dropped any rows where Date conversion failed.
- Finally, I extracted the Year as a new column.
---
## 2. Statistical Analysis
I applied .describe(include='all') to the cleaned dataset to summarize both numeric and categorical variables:
- Numeric variables like Speed_limit, Number_of_Vehicles, and Number_of_Casualties showed reasonable central tendencies:
  - Mean speed limit: 33.3 mph
  - Most accidents involved 2 vehicles and 1 casualty
- Date-based columns were converted and ranged from 1979 to 2018, with a median accident year around 1995
- Categorical variables like:
  - Gender: Most frequent = Male
  - Severity: Most frequent = Slight
  - Age_Grp: Most common = 11 to 15
  - Weather_conditions: Most common = Clear
  - Light_conditions: Most common = Daylight
  
These insights helped guide the visual analysis and were later used to formulate prescriptive safety recommendations.
---
## 3. Key Findings

1. Accidents per Year:
- An annual average of over 29,000 incidents were reported, thereby pointing to a period of high vulnerability; incidents peaked from 1983 through 1985.
- The downward trend between 1990 and 2010 was attributable to improved safety regulations and urban planning for road safety.
- After 2011, the trend seems to climb again and is probably a reflection of the increase in cyclists using a bike for commuting.
- Forty years of overall decline highlight the progress in traffic safety, but the recent increase shows that we need to refocus our efforts.
