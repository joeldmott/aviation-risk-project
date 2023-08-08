# Aviation Risk Assessment Project
## Project Overview:
The purpose of this project is to help a stakeholder make an informed decision to procure & operate low-risk airplanes.

### Data: The "Aviation Accident Database & Synopses, up to 2023" Kaggle dataset, found here:
https://www.kaggle.com/datasets/khsamaha/aviation-accident-database-synopses
This dataset is copied from the NTSB and "contains information from 1962 and later about civil aviation accidents and selected incidents within the United States, its territories and possessions, and in international waters." At the outsuet, it contained 88,889 records for various aircraft. By the end of this project, that is narrowed down to 31 recommended low-risk planes.

### Goals:
1. Evaluate data for aircraft safety records (fix duplicate or missing data, designate relevant & insightful measurement methods).
2. Recommend aircraft that are low-risk in terms of the	number & severity of incidents.
3. Categorize recommended planes in terms of size & cost.

### Methods overview:
First, I examined more general characteristics, such as aircraft manufacturers and the number of engines. This led me to recommend *against* lighter aircraft and those with only one engine. 
Then I compiled more specific findings, wherein I seperated the remaining 2+ engine planes into three categories based on seating capacity: private planes (seating 15 or fewer people), regional aircraft (seating 16-100), and large airliners (seating more than 100).

### Results overview:
Single-engine aircraft are involved in many more incidents than those with multiple engines. While there *are* more of these aircraft than the larger aircraft models, their omission from the recommended planes comes from the severity of their accidents. Even though they carry fewer people, they account for more injuries and fatalities than 2+ engine planes.
![image](https://github.com/joeldmott/aviation-risk-project/assets/51928528/666054ff-351d-4581-be1e-707e0ad0e4e0)

I then categorize planes by size because their fatality & injury counts differ substantially. Even among 2+ engine planes, private-size aircraft still account for more severe accidents. However, they are more affordable than regional or larger airliners, so their data is presented here instead of being omitted.
![image](https://github.com/joeldmott/aviation-risk-project/assets/51928528/3f5f8ddb-c7a3-4a2c-b9c7-4999736bfd6e)
In this data, 10.18% of private aircraft people were killed as opposed to 0.86% of regional people and 1.92% of larger airliner folks. So, I'd definitely recommend regional or larger airliners for a lower-risk approach to purchasing & operating aircraft.

Larger airline manufacturers are heavily consolidated, but these ten models represent the lowest-risk aircraft among this size:
![image](https://github.com/joeldmott/aviation-risk-project/assets/51928528/a4636fd6-0384-44dd-b090-4f83be71abc2)
Regional airliners are the safest overall:
![image](https://github.com/joeldmott/aviation-risk-project/assets/51928528/016650ea-875f-4c5e-a136-c5ae1d9c1cc6)
There are a lot more private aircraft models than there are regional or large airliners. In fact, a number of them have had no fatal or injury-involved accidents so far (even though private aircraft as a whole tell a different story).
Subsequently, I narrowed down these zero-injury planes further by their damage records. There are three damage categories in the NTSB dataset: minor, substantial, and destroyed. These are not equal, so I weighed them by severity. Every instance of a minor damage indicent is multiplied by 0.25, every substantial incident damage by 0.5, and every destroyed incident instance is left alone (multiplied by one). This results in a damage count that helped to refine the private aircraft to the point where I had twelve lowest-risk private planes:
![image](https://github.com/joeldmott/aviation-risk-project/assets/51928528/f7772fcc-983f-4620-824e-d9ae202689ed)


### Conclusions:
single-engine planes have a much higher-risk than planes with two or more engines
private aircraft are more affordable, but have more accidents
private aircraft accidents are deadlier overall
regional aircraft have the fewest accidents, but larger airliners are similarly safe

## Repository Structure:
├── images
├── .gitignore
├── AviationData.csv
├── README.md
├── Total Injuries and Fatalities by Regional Airliner
├── USState_Codes.csv
├── filtered_df_Model_column.csv
├── filtered_df_Model_column_finished.csv
├── project_notebook.ipynb
└── relevant_manufacturers.xlsx
