**Career Innings Filtration Using XRuns Prediction**
**Project Overview**
This project focuses on filtering and analyzing career innings of some of the top modern-day T20 cricketers using a custom-built model based on Expected Runs (XRuns). The model utilizes various match factors to predict the expected runs a batter might score on a particular ball. By comparing the actual runs scored (batruns) with the predicted XRuns, we calculate a metric called RAAR (Runs Above Average Replacement) to evaluate the batter's impact on the game.

**Files and Data**
**Key Files:**
_modelpred.csv:_ Contains ball-by-ball data for multiple T20 matches, including innings run rates, balls remaining, wickets down, and batter performances.
_ball_by_ball_expectedruns.cs_v: Output file after calculating XRuns for each ball.
_ball_by_ball_expectedruns_with_RAAR.csv:_ Output file with added RAAR column after comparing actual runs with XRuns.
_babar_azam_impact_innings.csv:_ A filtered dataset showcasing Babar Azam's impact innings.
_Babar Azam Powerplay Analysis CSVs:_ Data showing Babar's performances across different years and match formats (T20, T20I).
**Tools Used**:
_Python (Pandas):_ For data handling and manipulation.
_Google Colab: _For computation and dataset storage.
_Plotly:_ For creating interactive tables and visual summaries of player performances.
**Steps Involved:**
**1. Mounting Google Drive**
The project begins by mounting Google Drive to access the necessary CSV files.

**2. Calculating Expected Runs (XRuns)**
The Expected Runs (XRuns) were calculated using a Naive Average model that groups data based on inns_rr (innings run rate), inns_balls_rem (innings balls remaining), and inns_wkts (innings wickets). The average batter runs (batruns) were then computed for each group to estimate XRuns.
**
3. Calculating RAAR (Runs Above Average Replacement)**
After calculating XRuns, we computed RAAR as the difference between batruns and XRuns. This metric gives us an indication of whether a batter scored above or below the expected runs for that situation.

**4. Filtering Impact Innings (Babar Azam Example)**
We applied RAAR to filter out impact innings, where Babar Azam was used as a case study. By focusing on matches where he scored 100 or more runs, we extracted his significant contributions and created summaries for various years and match formats (T20, T20I).
**
**5. Analysis of Top T20 Batters****
A comprehensive filtration of innings was applied to a selection of top T20 batters, including names like Babar Azam, Virat Kohli, and Jos Buttler. Their innings were classified into categories like Failure, Cameo, Impact Innings, and Scoreboard Pressure Creating Innings based on their RAAR values and number of balls faced.

**Key Insights:**
RAAR helps identify not just high-scoring innings, but also the relative impact of those runs in the context of the game.
Powerplay Context: Special focus was given to performances in the powerplay overs (first 6 overs), analyzing how batters like Babar Azam performed in early innings situations.
Comparative Analysis: By applying the same model to multiple players, we were able to compare the relative effectiveness of their innings under different match conditions.
**Visualizations:**
Interactive tables and summaries were generated using Plotly, making it easier to explore the performances of different players over time and under various match circumstances.

**Future Directions:**
Extending the analysis to other T20 leagues and competitions.
Further refining the XRuns model by incorporating more detailed match context like opposition bowling strength and pitch conditions.
Adding visualization of cumulative RAAR across seasons to track the form and consistency of players.
