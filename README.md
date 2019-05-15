
# Columns meaning in the dataset
PER: Player Efficiency Rating/
GS: Games Started/
MP: Minutes Played/
TS%: True Shooting %/
FTr: Free Throw Rate
OWS: Offensive Win Shares
DWS: Defensive Win Shares
WS: Win Shares
WS/48: Win Shares Per 48 Minutes
FG%: Field Goal Percentage
2P%: 2-Point Field Goal Percentage
eFG%: Effective Field Goal Percentage
3P%: 3-Point Field Goal Percentage
FT%: Free Throw Percentage
3PA: 3-Point Field Goal Attempts
ORB%: Offensive Rebound Percentage
DRB%: Defensive Rebound Percentage
TRB%: Total Rebound Percentage
AST%: Assist Percentage
STL%: Steal Percentage
BLK%: Block Percentage
TOV%: Turnover Percentage
USG%: Usage Percentage
OBPM: Offensive Box Plus/Minus
DBPM: Defensive Box Plus/Minus
BPM: Box Plus/Minus
VORP: Value Over Replacement
FT: Free Throws
FTA: Free Throw Attempts
FG%: Field Goal Percentage


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
