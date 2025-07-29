# The analysis of bicycle-related accidents across the UK from 1979 to 2018
---
# Table of contents:
## 1. Exploratory Data Analysis (EDA)
### 2. Statistical Analysis
#### 3. Key Findings
##### 4.Dashboard Design


---
## 1. Exploratory Data Analysis (EDA)
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
I applied `.describe(include='all')` to the cleaned dataset to summarize both numeric and categorical variables:
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

<img width="1184" height="584" alt="1" src="https://github.com/user-attachments/assets/627c8959-dbc7-4eae-971b-249d90876871" />


2. Accident Severity by Gender:
- In more than 80% of the reported accidents, male cyclists were involved, pointing to a demographic trend in exposure.
- Most accidents fall under the category of "Slight" while Serious and Fatal accidents display the same male-biased pattern.
- Although female cyclists are few in number, they consistently maintain a presence and have a significantly lower severe incident ratio compared to male cyclists.
- Other genders accounted for almost no reports, which strongly indicates how non-inclusive data sets had been, especially in earlier decades.

<img width="784" height="484" alt="2" src="https://github.com/user-attachments/assets/96459e87-e3f1-4797-876f-aa6a59c5b128" />


3. Victims by Age Group:
- Moreover, children between 11 and 15 were the most prone, probably due to lower road experience and higher exposure during school travel.
- Adult riders between 26 and 45 make up a major share of the incidents, indicating elevated commuting activity within this population group.
- Elderly people (56 and above) sustain injuries less frequently, but when they do, they likely face a higher risk of serious injury.
- Even younger kids (6-10) appear in the data, and their occurrence indicates the need for early instruction in safety.

<img width="984" height="384" alt="3" src="https://github.com/user-attachments/assets/f2f22b70-aa78-4d37-8423-7f8e0eaef719" />


4. Weather & Light Conditions

*Weather Conditions:*
- More than 680,000 bicycle accidents take place during clear weather, which means the clear weather is the most favorable weather for bicycle accident occurrences.
- Rain stands second by frequency but shows quite a drop in its numbers (~80,000).
- Conditions like fog, snow, or winds are rarely heard of in the dataset.
- This means that environmental hazards account for only a few accidents, while most accidents involve cyclists losing control in good weather conditions.

*Light Conditions:*
- Most of the incidents take place during the day (~650,000).
- Conversely, even when the lights are on and the darkness persists, approximately 140,000 accidents still occur, indicating that the lights have not fully mitigated the risk.
- In total darkness with no lights, the accidents are few (~30,000), although probably the worst.
- This perhaps means visibility is not the limiting factor but rather some infrastructural or behavioral issues.

<img width="1583" height="484" alt="4" src="https://github.com/user-attachments/assets/fa1b28ed-6013-4b96-a3b8-9a79fdc827aa" />

---

## 4.Dashboard Design
This Jupyter-based dashboard is structured, interactive, and user-friendly:
- Organized into clear sections: data preview, cleaning, visual insights, and interactive filtering.
- Includes a dropdown menu to explore severity by gender across years, making it dynamic and engaging.
- Charts are well-labeled, colors are bright, and confident style is maintained.

<img width="813" height="422" alt="Screenshot 2025-07-28 at 3 52 18 PM" src="https://github.com/user-attachments/assets/f0261a44-c5ee-4496-b19b-8e65181a60bf" />

