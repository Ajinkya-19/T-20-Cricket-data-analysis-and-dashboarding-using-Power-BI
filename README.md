
# T-20-Cricket-data-analysis-and-dashboarding-using-Power-BI


this project is focused on create best 11 based on the players weakness and Power.The objective of this project is to assemble the best 11-player team for T20 World Cup. Comprehensive insights from the 2022 T20 World Cupvdata are required to make informed decisions on player selection.

In this project I scraped data from the ESPNcricinfo website
using Bright Data, transform and clean the data with pandas, and created
a detailed dashboard in Power BI. This dashboard will help in identifying
the best-performing players.



## 🛠 Skills
* Python
*  Pandas
*  Numpy
*   PowerBi
*    webscraping
* Data collection
*  Data Preprocessing
*   Deeper analytical mindset
## Working
 In this section I Describe the working of the project.
    1) convert the json file into data frame then performing data preprocessing and data cleaning process on them.
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
1. Modelling
![Modelling](https://github.com/user-attachments/assets/2eab8eb5-e452-4350-96c5-22e448cd0c77)
2. Power Hitters/ Openers
![Openers](https://github.com/user-attachments/assets/cc4c038d-fcbc-4893-9fef-25e2b41bafb5)
3.Anchors/Middle order Batsman
![Anchors](https://github.com/user-attachments/assets/1a59c434-041a-4fca-b2b2-a9646c7a4a9a)
4.finisher
![Finisher](https://github.com/user-attachments/assets/1abb0962-f9a8-47ac-a219-8675686f8fe8)
5.All Rounders
![All Rounders](https://github.com/user-attachments/assets/0d2c1421-7893-4ea0-b978-716d38e63fe8)
6. Specialist Fast ballers
![Fast Ballers](https://github.com/user-attachments/assets/1d523698-70fa-4727-b5db-2c78e4ad415d)
7. Best Final 11 
![Best 11](https://github.com/user-attachments/assets/125f17ec-146e-45f5-ada0-d1665043cb8a)

## Demo
https://github.com/user-attachments/assets/ef10d1a7-31e8-44d5-8ff2-e2b6c75e0832

## Final Best 11
|Position|Player Name| Team|Player Role|
|:----------|:-----------|:---------|:-----|
|1|Jos Buttler|England|Wicketkeeper batsman|
|2|Rilee Rossouw|South Africa|Top order Batter|
|3|Virat Kohli|India|Top order Batter|
|4|Suryakumar Yadav|India|Batter|
|5|Glenn Phillips|New Zealand|Wicketkeeper Batter|
|6|Marcus Stoinis|Australia|Batting Allrounder|
|7|Sikandar Raza|Zimbabwe|Batting Allrounder|
|8|Shadab Khan|Pakistan|Allrounder|
|9|Sam Curran|England|Allrounder|
|10|Shaheen Shah Afridi|Pakistan|Bowler|
|11|Anrich Nortje|South Africa|Bowler|

## This is the final 11 of analyzing 500-600 players from 11 countries and this best 11 which creates significant effects in any tournament and matches.

# Author- Ajinkya Chavan
# Github Account-Ajinkya-19

