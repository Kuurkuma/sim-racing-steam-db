# Sim-racing data analysis

![Global trend](reports/figures/01-line_chart-global_trend.png)


**Embarking on the journey to delve into the world of sim-racing games, here are two key objectives to achieve:**

- Exploring historical trends in sim-racing games on Steam.
- Integrating real-time data from various platforms to capture current patterns and player activity

# Historical trends

## Introduction
The analysis aims to explore the historical trends of racing simulation games on the Steam platform between 2013 and 2023. The hypothesis posits that sim-racing games are experiencing increasing popularity over time.

## Background
The Steam database serves as a rich source of historical gaming data, offering insights into user preferences and trends over time. By focusing on the top 10 "Automobile Sim" games on Steam from 2013 to 2023, provided in .csv format by the SteamDB website, we seek to unravel patterns and fluctuations in the popularity of racing simulation games.

## Tools used:

- Python: as the language for this project, using Pandas for data manipulation and analysis, and Plotly for creating interactive visualizations.
- Streamlit: To build an user-friendly dashboard.
- Git & GitHub: Git for version control system & GitHub for tracking changes.

## Analysis
Our analysis commences with an in-depth examination of historical data retrieved from the Steam platform. Through the exploration of Steam database records, we aim to identify trends, shifts, and recurrent patterns in the popularity of racing simulation games over the past decade.

### 01. How average active players is evolving over time?
We see a global positive trend in the last 10 years.
There was a huge peak in December 2014 with 21'620 players on average.
But zooming on the year 2023, we see the average players stay relatively steady, even dropping until 5400k players in December 2023.

![2023_trend](reports/figures/line_chart-global_trend_2023.png)

### 02. How is the Twitch viewership for sim racing games changing?
February 2016 and November 2021 saw huge peaks in twitch viewers. Since, 2021, the average viewers per game has been decreasing.

![global_viewvers](reports/figures/line_chart-global_trend_viewers.png)

### 03. What is the trend in the average player count per game over time?
Head-to-head:

- Assetto Corsa Competizione vs Automobilista 2:
Assetto Corsa Competizione has a way higher player base than Automobilista 2.

![acc_auto2](reports/figures/line_chart-acc-automob.png)


- Euro truck 2 vs American simulator:
Euro truck has a bigger & a constant growing active player community despite a a fall at the end of 2023.
American truck has a smaller but steady player base.

![euro_american](reports/figures/line_chart-euro-american_truck.png)

- Forza horizon 4 VS Forza horizon 5:
Despite being the older game, FH 4 keeps a certain popularity among Steam players.

![fh4_fh5](reports/figures/line_chart-fh4-fh5.png)


- Assetto Corsa vs BeamNG:
Assetto Corsa and BeamNG has a similar player base. Since the launch, Assetto Corsa was the most popular but in August 2019, BeamNG became more popular.
It maintained a higher player based until now.

![assetto_beam](reports/figures/line_chart-asetto-beam.png)

- Car X drift vs Dirt rally 2.0:
Dirt Rally 2.0 was a more popular game until Q1 of 2021 where Car X got more active player. since then, Dirt only lost in popularity, when Car X drift maintained a higher player base.

![carX_dirt2](reports/figures/line_chart-carX-dirt2.png)


### 04. What is the game with the most active players?
Euro truck 2 is on average the game with the most active players of the last decade (2013-2023), followed by Forza horizon 5 & BeamNG.

![avg_players](reports/figures/bar_plot-avg_player_game.png)


### 05. Which games attracts most twitch viewers ?
For viewers, Forza Horizon 5 take the first place, followed by Euro truck simulator 2 and Forza horizon 4.

![avg_viewers](reports/figures/bar_plot-avg_viewer_game.png)

### 06. Is there a correlation between average players count & twitch viewers ?
There is no clear correlation between active players & Twitch viewers.

![player_viewer](reports/figures/scatter_players_viewers.png)


### 07. Which day players are the most active ? less active?
As anticipated, weekends tend to attract the highest number of players, with Sunday being the peak day.
On the other hand, Wednesdays typically see fewer players on average.

![avg_days](reports/figures/bar_plot-avg_players_day.png)

### 08. What is the distribution of twitch viewers per month in the last 3 years?
In 2021 and 2022, June and November emerged as the peak months for Twitch viewership.
For 2023, March was the busiest month.

![violin_viewer](reports/figures/violin_viewers.png)

## Conclusion

Through our analysis of Steam automobile simulation racing games over the last decade, we've gained valuable insights into player trends and community preferences.
By examining gameplay data and Twitch viewership, we've identified the most popular games within the community.
Additionally, we've delved into average player engagement on a daily and monthly basis.
However, for a more comprehensive understanding of sim racing behaviors, we recognize the importance of incorporating data from other platforms such as iRacing
and exploring additional player demographics like location, age, and gender.

## Limitations

- Our dataset is limited to the Steam marketplace, excluding major sim racing games such as iRacing.
- Certain games categorized as "Automobile sim racing" may not strictly align with traditional sim racing titles (CarX and the Forza Horizon series.)
- The frequency of player count records is restricted to once per day throughout our analysis period.
- Lack of Demographic Data: Absence of demographic information (e.g., age, gender, location) limits the understanding of player demographics and preferences.

---

## 2. Create an interactive dashboard using Plotly & Streamlit

After gathering and processing the data from SteamDB, we use Plotly and Streamlit to build an interactive dashboard. This dashboard provides an exploration of trends and patterns identified in our analysis.
With Plotly's powerful visualization capabilities and Streamlit's user-friendly interface, users will be able to interact with the data, gaining insights into the popularity of sim-racing games over the years.

---

## 3.Integration of real-time data from various platforms via API calls:
(_This will be part of an other project_)
We will then exploit real-time data streams from other services, including Steam, iRacing, marketplaces and publisher platforms.

By leveraging the APIs provided by these platforms, we will have access to hourly player counts and more accurate information on current trends.

Through the combined analysis of historical data and real-time information, we hope to gain a comprehensive understanding of the past and present popularity of racing simulation games, and thus answer the hypothesis posed.
