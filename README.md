# PWC Virtual Work Experience - Call Centre Trends


## Problem Statement
Create a dashboard in Power BI that reflects all relevant Key Performance Indicators (KPIs) and metrics in the dataset.

#### Possible KPIs include (but not limited to):

- Overall customer satisfaction
- Overall calls answered/abandoned
- Calls by time
- Average speed of answer
- Agent’s performance quadrant

## Data Source
Dataset : 
[01 Call-Center-Dataset.xlsx](https://github.com/Athira-AM/Call-center-trend-analysis/files/14064852/01.Call-Center-Dataset.xlsx)

## Data Preparation
The Call Center Trends dataset, containing 10 columns and 5000 rows, was prepared in Power Query Editor within Microsoft Power BI Desktop. The aim was to ready the dataset for modeling and analysis.

#### Data Cleaning Steps :

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

## Data Visualization (Dashboard)
| Call Centre Trends |
| ----------- |
|![Call center dashboard](https://github.com/Athira-AM/Call-center-trend-analysis/assets/157714268/5b7fe475-f318-47d1-8f04-a4dab7fe840d)|

## Insights :

1. **Satisfaction Rate** : Customers seem moderately satisfied, with an average rating of 3.4 out of 5. 

2. **Call Handling** : More calls are being answered than unanswered, showing that the call center is doing well in managing incoming calls.

3. **Agent Speed** : Joe is the quickest at answering calls, which is great for efficiency.

4. **Popular Topics** : Most calls are about Streaming and Technical support, indicating areas where more attention might be needed.

5. **Agent Performance** : Martha has the happiest customers, while Jim handles a lot of calls and resolves many issues.

6. **Issue Resolution** : Admin support resolves more calls and more unresolved calls are in Technical support.

7. **Resolution Trends** : January had the highest issue resolution rate, dipping in February but rising again in March. This shows some ups and downs in solving problems over time.


## Recommendations based on the insights :

- **Train Agents Better** : Provide more training to agents on how to handle calls effectively and make customers happier.

- **Direct Calls Smarter** : Use technology to make sure calls go to the right agents quickly, reducing waiting times for customers.

- **Get More Tech Help** : Since a lot of calls are about technical issues, consider hiring more tech support staff or giving extra training to current staff.

- **Reward Good Work** : Give bonuses or rewards to agents who answer calls quickly, solve problems well, and keep customers satisfied.

- **Give Feedback Regularly** : Have regular meetings with agents to talk about how they're doing and give tips on how to improve.

- **Watch Call Trends** : Keep an eye on what kinds of calls are coming in most often, so you can fix common problems.

- **Ask Customers What They Think** : Get feedback from customers after calls to find out what went well and what could be better.



    
  


