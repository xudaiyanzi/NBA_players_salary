
# Background
This project aims to explore how a variety of factors can be used to predict the salary of the NBA players from 1999-2019. Our goals for this project:
1)	Salary prediction (discover which factors are the best predictors of an NBA player’s salary, using regression model to predict salaries).
2)	Using cluster model to find out similarity or categorizing players (for example, utilizing physical characteristics data to predict performance of NBA players).
3)	Determine which players have been overvalued and undervalued according to their given vs. predicted salary.
# Input datasets
We plan to get out input data from the following sources:
1)	Physical characteristics of the 1996~2016 NBA players
https://www.kaggle.com/justinas/nba-players-data/downloads/nba-players-data.zip/2 (CSV format)
2)	Data for injuries
https://www.kaggle.com/ghopkins/nba-injuries-2010-2018 (CSV format)
3)	NBA Player Stats since 1950
https://www.kaggle.com/drgilermo/nba-players-stats (CSV format)
4)	NBA Player Salary Data 2002/03 - 2017/18
https://www.kaggle.com/hultm28/nba-player-salary-data-2002-2017 (CSV format)
The average NBA salary has drastically increased over the past 20 years. The solution is to normalize salary data by putting it as a percentage of the league’s salary cap, the total salary limit that a team can spend on its players in a given season. The salary cap has risen as player salaries have.
# Possible skills
•	Python Pandas
•	Python Matplotlib
•	Tableau

# Columns meaning in the dataset
PER: Player Efficiency Rating/
GS: Games Started/
MP: Minutes Played/
TS%: True Shooting %/
FTr: Free Throw Rate/
OWS: Offensive Win Shares/
DWS: Defensive Win Shares/
WS: Win Shares/
WS/48: Win Shares Per 48 Minutes/
FG%: Field Goal Percentage/
2P%: 2-Point Field Goal Percentage/
eFG%: Effective Field Goal Percentage/
3P%: 3-Point Field Goal Percentage/
FT%: Free Throw Percentage/
3PA: 3-Point Field Goal Attempts/
ORB%: Offensive Rebound Percentage/
DRB%: Defensive Rebound Percentage/
TRB%: Total Rebound Percentage/
AST%: Assist Percentage/
STL%: Steal Percentage/
BLK%: Block Percentage/
TOV%: Turnover Percentage/
USG%: Usage Percentage/
OBPM: Offensive Box Plus/Minus/
DBPM: Defensive Box Plus/Minus/
BPM: Box Plus/Minus/
VORP: Value Over Replacement/
FT: Free Throws/
FTA: Free Throw Attempts/
FG%: Field Goal Percentage/


# player_stats_df should be a on a per-game basis instead of totals to eliminate the effect of games played

player_stats_df["MPG"]=player_stats_df["MP"]/player_stats_df["GP"]
player_stats_df["ORPG"]=player_stats_df["ORB"]/player_stats_df["GP"]
player_stats_df["DRPG"]=player_stats_df["DRB"]/player_stats_df["GP"]
player_stats_df["RPG"]=player_stats_df["TRB"]/player_stats_df["GP"]
player_stats_df["APG"]=player_stats_df["AST"]/player_stats_df["GP"]
player_stats_df["SPG"]=player_stats_df["STL"]/player_stats_df["GP"]
player_stats_df["BPG"]=player_stats_df["BLK"]/player_stats_df["GP"]
player_stats_df["TPG"]=player_stats_df["TOV"]/player_stats_df["GP"]
player_stats_df["PFPG"]=player_stats_df["PF"]/player_stats_df["GP"]
player_stats_df["PPG"]=player_stats_df["PTS"]/player_stats_df["GP"]
player_stats_df["FGPG"]=player_stats_df["FG"]/player_stats_df["GP"]
player_stats_df["FGAPG"]=player_stats_df["FGA"]/player_stats_df["GP"]
player_stats_df["3PPG"]=player_stats_df["3P"]/player_stats_df["GP"]
player_stats_df["3PAPG"]=player_stats_df["3PA"]/player_stats_df["GP"]
player_stats_df["2PPG"]=player_stats_df["2P"]/player_stats_df["GP"]
player_stats_df["2PAPG"]=player_stats_df["2PA"]/player_stats_df["GP"]
player_stats_df["FTPG"]=player_stats_df["FT"]/player_stats_df["GP"]
player_stats_df["FTAPG"]=player_stats_df["FTA"]/player_stats_df["GP"]
