
# T-20-Cricket-data-analysis-and-dashboarding-using-Power-BI


this project is focused on craete best 11 based on the players weakness and Power.The objective of this project is to assemble the best 11-player team for T20 World Cup. Comprehensive insights from the 2022 T20 World Cupvdata are required to make informed decisions on player selection.

In this project I scraped data from the ESPNcricinfo website
using Bright Data, transform and clean the data with pandas, and created
a detailed dashboard in Power BI. This dashboard will help in identifying
the best-performing players.



## 🛠 Skills
Python,Pandas,Numpy,PowerBi,webscraping, Data collection,Data Preprocessing,Deeper analytical mindset
## Working
 In this section I Describe the working of the project.
    1) convert the json file into data frame then performing data preprocessing and data cleaning process on them.|
    2) convert the data set int csv file and open into Power-Bi software.
    3) In power query section performing data cleaning once again and the in Dax section create data modelling which shown below.
    4) at last stage carete a Report based on the condition, in Which create best 11 from dimplayer, batsman, Ballers, Allrounders.


## Condition 
For Create best 11 from more than 500-600  players I decided some Conditions for Team, Openrs, middle orders batsman, Lower order Batsman tail enders, fast Ballers etc.
# Team
1.The team should be able to score at
least 180 runs on an average.

2.They should be to defend 150 runs
on an average.

# Openrs
|PARAMETERS| DESCRIPTION | CRITERIA |
| :--------| :--------| :--------|
|Batting Average|Average runs scored in an innings |> 30|
|Strike Rate| No of runs scored per 100 balls|> 140|
|Innings Batted| Total Innings batted |> 3|
|Boundary % |% of runs scored in boundaries |> 50|
|Batting Position| Order in which the batter played| < 4|

# MIDDLE ORDER
|PARAMETERS| DESCRIPTION | CRITERIA |
| :--------| :--------| :--------|
|Batting Average| Average runs scored in an innings| > 40|
|Strike Rate| No of runs scored per 100 balls| > 125|
|Innings Batted| Total Innings batted| > 3|
|Avg. Balls Faced|Average balls faced by the batter in an innings|>20|
|Batting Position| Order in which the batter played |> 2|

# FINISHER
|PARAMETERS| DESCRIPTION | CRITERIA |
| :--------| :--------| :--------|
|Batting Average| Average runs scored in an innings| > 25|
|Strike Rate| No of runs scored per 100 balls| > 130|
|Innings Batted| Total Innings batted|> 3|
|Avg. Balls Faced| Average balls faced by the batter in an innings|> 12|
|Batting Position| Order in which the batter played |> 4|
|Innings Bowled| Total Innings Bowled by the bowler| > 1|

# ALL-ROUNDERS /LOWER ORDER
|PARAMETERS| DESCRIPTION | CRITERIA |
| :--------| :--------| :--------|
|Batting Average| Average runs scored in an innings| > 15|
|Strike Rate| No of runs scored per 100 balls| > 140|
|Innings Batted| Total Innings batted|> 2|
|Batting Position|Order in which the batter played|> 4|
|Innings Bowled| Total Innings bowled|> 2|
|Bowling Economy|Average runs allowed per over| < 7|
|Bowling Strike Rate |Average no. of balls required to take a wicket |< 20|

# SPECIALIST FAST BOWLERS
|PARAMETERS| DESCRIPTION | CRITERIA |
| :--------| :--------| :--------|
|Innings Bowled |Total Innings bowled| > 4|
|Bowling Economy| Average runs allowed per over |< 7|
|Bowling Strike Rate|Average no. of balls required to take a wicket|< 16|
|Bowling Style| Bowling style of the player|%%Fast%%|
|Bowling Average| No. of runs allowed per wicket| < 20|
|Dot Ball % |% of dot balls bowled |> 40|

## DAX Formulas

To  finalised the best 11 in Power bi I created some Dax Formulas but I provide some of the formulas . I will provide the list of formulas in repository.
|Sno|	Measures|	Description / Purpose|	DAX FORMULA|
|:---|:---------|:-----------------------|:-----------|
|1|	Total Runs|	Total number of runs scored by the batsman|	Total Runs = SUM(fact_batting_summary[runs])|	
|2|	Total Innings Batted|Total number of innings a batsman got a chance to bat|	Total Innings Batted = COUNT(fact_batting_summary[match_id])|	
|3|Total Innings Dismissed|To find the number of innings batsman got out|SUM(fact_batting_summary[out])	|
|4|Batting Average|	Average runs scored in an innings|	Batting Avg = DIVIDE([Total Runs],[Total Innings Dismissed],0)|	
|5|Strike Rate|	No of runs scored per 100 balls|	Strike rate = DIVIDE([Total Runs],[total balls faced],0)*100|

## Screenshots


![Screenshot 2024-08-23 230147](https://github.com/user-attachments/assets/2f827ab9-2446-450e-aa89-4e324a3ae7e2)



![Screenshot 2024-08-24 002346](https://github.com/user-attachments/assets/a3f3e3b9-a5b8-4647-98ac-54c038b1c839)



![Screenshot 2024-08-24 002429](https://github.com/user-attachments/assets/3bdd1845-1657-4c71-a70b-5c1e74c719c8)



![Screenshot (121)](https://github.com/user-attachments/assets/f60f0883-695d-4238-967d-52f1ec8cb60a)



![Screenshot 2024-08-24 002246](https://github.com/user-attachments/assets/c4b2208b-4fd5-421d-a8de-44bf1db0b3a2)


