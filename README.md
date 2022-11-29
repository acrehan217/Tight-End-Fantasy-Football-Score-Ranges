# Tight-End-Fantasy-Football-Score-Ranges
Analysis of NFL tight end fantasy football performance from the 2020-2022 seasons

Executive Summary
This dataset represents the stats of NFL quarterbacks, running backs, wide receivers, and tight ends, by week, during the 2020, 2021, and 2022 seasons (through Week 9) and contracts signed by free agents during the 2020, 2021, and 2022 off-seasons. Imagine you are in the playoff hunt in your fantasy football league – you desperately need a win this week. You’re trailing your matchup by eight points heading into Monday Night Football with only one player left to play. You have a rookie running back or a veteran wide receiver, both are projected to score ten points. Who do you put in your lineup? In this instance, while the projected score is helpful, an analysis of those players’ range of scores would be much more beneficial. It’s great to know what a player’s most likely outcome is, but what if they have a great game? What if they have a horrible game? Examining player score spreads could be very beneficial for fantasy football managers.

DATA SOURCES
•	Player stats and contract data obtained from NFL.com.

•	Marginal tax rates obtained from turbotax.com. 

LIMITATIONS AND ETHICS
•	Player’s on-field performance is often a product of their environment. If the star quarterback gets hurt or a coach gets fired, the player’s performance will be affected. The impact of changing surroundings is not evident in the data.
•	Each position has a minimum number of “attempts” to be included in the analysis:
o	QB: 200 passes
o	RB: 100 carries
o	WR and TE: 50 receptions.
•	Player contracts are often heavily incentivized and not always guaranteed. The reported number and the actual compensation to a player often vary depending upon the specific contract and performance.
•	Only free-agent contracts exceeding $10,000,000 were included in the analysis.
DATA CLEANING AND CONSISTENCY CHECKS
•	Adjust data type.
•	Eliminate players with too few attempts.
•	Derive fantasy points for all three scoring formats, standard or 0 points per reception (PPR), 0.5 PPR, and 1 PPR, scored from player’s stats.
•	Derive estimated state income tax using contract value and highest marginal tax bracket per the state in which a team plays their home games.
•	Check for missing data.
•	Check for duplicates.
•	Did not look for presence of outliers. In football outliers are part of the game – the best players can have horrible games and the worst players can have great games. Any “outliers” remained in the dataset. 

DATA PROFILE
Dataset number of rows and columns:
•	Final_QB: 1267x18
•	Final_RB: 2400x20
•	Final_WR: 3325x19
•	Final_TE: 1375x19
•	Final_FA: 174x7
•	QB: 1391x18 (raw dataset)
•	RB: 3402x20 (raw dataset)
•	WR: 4735x19 (raw dataset)
•	TE: 2300x19 (raw dataset)
•	FA: 174x5 (raw dataset)

COLUMN DETAILS
Final_QB:
Column	Column Description	Data Type	Time Variant?
YEAR	NFL Year	Quantitative, Discrete	Yes
WEEK	Week of NFL Season	Quantitative, Discrete	Yes
RANK	Weekly position rank	Quantitative, Discrete	No
PLAYER	Player name	Qualitative, Nominal	No
CMP	Number of completions	Quantitative, Discrete	No
PASS ATT	Number of passing attempts	Quantitative, Discrete	No
PCT	Completion percentage	Quantitative, Continuous	No
PASS YDS	Passing yards	Quantitative, Discrete	No
Y/A	Yards per passing attempt	Quantitative, Continuous	No
PASS TD	Passing touchdowns	Quantitative, Discrete	No
INT	Interceptions	Quantitative, Discrete	No
SACKS	Sacks	Quantitative, Discrete	No
RUSH YDS	Rushing yards	Quantitative, Discrete	No
RUSH TD	Rushing touchdowns	Quantitative, Discrete	No
FL	Fumbles lost	Quantitative, Discrete	No
G	Games played	Quantitative, Discrete	No
FPTS	Fantast points	Quantitative, Continuous	No

Final_RB:
Column	Column Description	Data Type	Time Variant?
YEAR	NFL Year	Quantitative, Discrete	Yes
WEEK	Week of NFL Season	Quantitative, Discrete	Yes
RANK	Weekly position rank	Quantitative, Discrete	No
PLAYER	Player name	Qualitative, Nominal	No
ATT	Rushing attempts	Quantitative, Discrete	No
RUSH YDS	Rushing yards	Quantitative, Discrete	No
Y/A	Yards per rushing attempt	Quantitative, Continuous	No
LG	Longest rush	Quantitative, Discrete	No
20+	Rushes of 20+ yards	Quantitative, Discrete	No
RUSH TD	Rushing touchdowns	Quantitative, Discrete	No
REC	Receptions	Quantitative, Discrete	No
TGT	Targets	Quantitative, Discrete	No
REC YDS	Receiving yards	Quantitative, Discrete	No
Y/R	Yards per reception	Quantitative, Continuous	No
REC TDS	Receiving touchdowns	Quantitative, Discrete	No
FL	Fumbles lost	Quantitative, Discrete	No
G	Games played	Quantitative, Discrete	No
0 PPR	0 PPR scoring format	Quantitative, Continuous	No
.5 PPR	.5 PPR scoring format	Quantitative, Continuous	No
1 PPR	1 PPR scoring format	Quantitative, Continuous	No

Final_WR:
Column	Column Description	Data Type	Time Variant?
YEAR	NFL Year	Quantitative, Discrete	Yes
WEEK	Week of NFL Season	Quantitative, Discrete	Yes
RANK	Weekly position rank	Quantitative, Discrete	No
PLAYER	Player name	Qualitative, Nominal	No
REC	Receptions	Quantitative, Discrete	No
TGT	Targets	Quantitative, Discrete	No
REC YDS	Receiving yards	Quantitative, Discrete	No
Y/R	Yards per reception	Quantitative, Continuous	No
LG	Longest reception	Quantitative, Discrete	No
20+	Receptions of 20+ yards	Quantitative, Discrete	No
REC TDS	Receiving touchdowns	Quantitative, Discrete	No
ATT	Rushing attempts	Quantitative, Discrete	No
RUSH YDS	Rushing yards	Quantitative, Discrete	No
RUSH TD	Rushing touchdowns	Quantitative, Discrete	No
FL	Fumbles lost	Quantitative, Discrete	No
G	Games played	Quantitative, Discrete	No
0 PPR	0 PPR scoring format	Quantitative, Continuous	No
.5 PPR	.5 PPR scoring format	Quantitative, Continuous	No
1 PPR	1 PPR scoring format	Quantitative, Continuous	No

Final_TE:
Column	Column Description	Data Type	Time Variant?
YEAR	NFL Year	Quantitative, Discrete	Yes
WEEK	Week of NFL Season	Quantitative, Discrete	Yes
RANK	Weekly position rank	Quantitative, Discrete	No
PLAYER	Player name	Qualitative, Nominal	No
REC	Receptions	Quantitative, Discrete	No
TGT	Targets	Quantitative, Discrete	No
REC YDS	Receiving yards	Quantitative, Discrete	No
Y/R	Yards per reception	Quantitative, Continuous	No
LG	Longest reception	Quantitative, Discrete	No
20+	Receptions of 20+ yards	Quantitative, Discrete	No
REC TDS	Receiving touchdowns	Quantitative, Discrete	No
ATT	Rushing attempts	Quantitative, Discrete	No
RUSH YDS	Rushing yards	Quantitative, Discrete	No
RUSH TD	Rushing touchdowns	Quantitative, Discrete	No
FL	Fumbles lost	Quantitative, Discrete	No
G	Games played	Quantitative, Discrete	No
0 PPR	0 PPR scoring format	Quantitative, Continuous	No
.5 PPR	.5 PPR scoring format	Quantitative, Continuous	No
1 PPR	1 PPR scoring format	Quantitative, Continuous	No

Final_FA:
Column	Column Description	Data Type	Time Variant?
Year	NFL Year	Quantitative, Discrete	Yes
Player	Player name	Qualitative, Nominal	No
From	Team losing free agent	Qualitative, Nominal	No
To	Team gaining free agent	Qualitative, Nominal	No
Value (Ms)	Contract value in millions	Quantitative, Continuous	No
Tax Rate	Highest state income tax bracket in state in which team plays their home games	Quantitative, Continuous	No
Tax Est (Ms)	Estimated tax liability in millions	Quantitative, Continuous	No

QUESTIONS TO EXPLORE
•	What does the spread of NFL players’ fantasy scores look like? Does it differ by position? What is the connection between player value and scoring consistency?
•	Do players consider state income tax when deciding whom to sign with during free agency?
