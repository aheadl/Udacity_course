# Udacity_course
<b>Introduction</b>
Dataset Description
The datasets used in this project reside in a database with 7 tables (listed below), which have data on the European Soccer leagues:

Country
League
Match
Player
Player_Attributes
Team
Team Attributes
The data in the tables includes 25,000 matches, 11,000 players, 11 European leagues, covering seasons (2008 to 2016), players and teams and their attributes. Some of the data includes details on matches played, goals scored (by home and away teams), penalties, other player statistics, and betting odds by betting providers. Once I familiarize myself with the data, my analysis will focus on the data that will contribute the most to what I would like to report on. One of the reasons I chose to work with data which originates from a database is to brush up on my SQL skills, which I have not used in quite a few years.

The relationships between tables are as follows:

Country, League and Match tables:
The Country table has a list of 11 countries that represents the European soccer league, as well as the country's id.
The League table has the names of the different leagues in Europe and their country ids
The Match table has the matches played from 2008 to 2016 in the European leagues, as well as the league id, country id, home and away goals, and team ids and provider bets (home, away, draw odds)
These three tables have country_id fields which will allow the tables to be joined to get information on matches played, the home and away team ids, goals scored by home and away teams, the leagues that the teams are associated with and the countries Country (id, name) & League (id, country_id, name) relationship is
Country.id = League.id & League.country_id = Match.country_id;

Player and Player_Attributes tables:
The combined tables provide information on the players, such as their names, biometric and detailed soccer related statistics, some of which are possessions, penalties, dribbling, sprint speed, agility, passing reactions, e.t.c :

Both tables have the same player_api_id and player_fifa_api_id fields, thus allowing them to be joined to provide extensive data on players, i.e.
Player.player_api_id = Player_Attributes.player_api_id,
Player.player_fifa_api_id = Player_Attributes.player_fifa_api_id
The fields chosen from Player were - id, player_api_id, player_name, player_fifa_api_id, birthday, height, weight.
The fields chosen from Player_Attributes include fields that are also in the Player tables, as well as the extensive list of fields which have players' game statistics, as listed above.

Team and Team_Attributes tables:
The Team table provides information on the names of the teams in the 11 leagues, and their team and league ids - id, team_api_id, team_fifa_api_id, team_long_name, team_short_name.
The Team_Attributes table provides additional information on each team, which includes statistics such as buildup play speed, playclass, buildup play dribbling and class, passing, passing class, defence pressure, aggression, team width.
Both tables have team_api_id and team_fifa_api_id, which were used to merge them.

Additionally, the Team and Match tables can be joined to get information on the matches the home/away teams are affiliated with as well as the goals scored by team. This merger can be further extended to merge with the League table to include any associations with leagues.

Summary of analysis:
I will be analyzing the data associated with each table and will be interested in looking at the following items, and providing a report:

Total home/away goals scored by each league over time - will include a graph showing highest and lowest total goals over the time span
The season with the highest/lowest, home/away goals and by which leagues
Teams with the most goals over time
Highest rated soccer player, as well as top 5 highest rated soccer players
Player with the most penalties, as well as the top 5 players with the highest penalties
Average goals per league over time
