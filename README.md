# PWC Virtual Work Experience - Call Centre Trends

## Problem Statement :
Create a dashboard in Power BI that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

#### Possible KPIs include (but not limited to):

- Overall customer satisfaction
- Overall calls answered/abandoned
- Calls by time
- Average speed of answer
- Agent’s performance quadrant 

## Data Preparation
The Call Center Trends dataset, containing 10 columns and 5000 rows, was prepared in Power Query Editor within Microsoft Power BI Desktop. The aim was to ready the dataset for modeling and analysis.

### Data Cleaning Steps :

1. #### Value Replacement :
   - The "Answered (Y/N)" column was adjusted for clarity, with "N" and "Y" values replaced with "No" and "Yes," respectively.
2. #### Error Removal :
   - Identified and removed errors present in the dataset to maintain data accuracy and reliability.
3. #### Data Type Validation :
   - Validated each column to ensure the correct data type was assigned. 
4. #### Datetime Transformation :
   - The "AvgTalkDuration" column originally contained both time and date information. To focus specifically on duration, the data type was adjusted to represent only time.

## Data Analysis (DAX)

  - Total calls = `COUNT(Call_centre_data[Answered (Y/N)])`
    
  - Total calls answered = `COUNTROWS(FILTER(Call_centre_data,Call_centre_data[Answered (Y/N)]= "Yes"))`
    
  - Total calls unanswered = `COUNTROWS(FILTER(Call_centre_data,Call_centre_data[Answered (Y/N)]= "No"))`
    
  - Total resolved calls = `COUNTROWS(FILTER(Call_centre_data,Call_centre_data[Resolved]= "Yes")) `
    
  - Total unresolved calls = `COUNTROWS(FILTER(Call_centre_data,Call_centre_data[Resolved]= "No")) `
    
  - Average satisfaction rate = `AVERAGE(Call_centre_data[Satisfaction rating])`
    
  - Average speed of answering (In sec) = `AVERAGE(Call_centre_data[Speed of answer in seconds])`

## Data Visualization
![Call center dashboard](https://github.com/Athira-AM/Call-center-trend-analysis/assets/157714268/5b7fe475-f318-47d1-8f04-a4dab7fe840d)

 
    
    
  


