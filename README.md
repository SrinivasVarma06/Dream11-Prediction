# Dream11-Prediction

Input (Playing XI):
  Took an Excel file with the playing XI for a specific match.
  Each player had a role (BAT, BOWL, WK, ALL).

Web Scraping:
  For each player, used their unique ESPN Cricinfo ID to scrape:
  Batting stats (e.g., Runs, 4s, 6s, SR)
  Bowling stats (e.g., Wickets, Economy)
  Fielding stats (e.g., Catches, Stumpings)

Feature Engineering:
  Cleaned and preprocessed raw stats.
  Applied a 3-match moving average to smooth noisy data.

Prediction:
  Used lag-1 Linear Regression (simple autoregression) to forecast next-match stats for each player.

Scoring:
  Applied official Dream11 scoring rules to predicted stats.
  Calculated a total Dream11 score for each player.

Team Selection Logic:
  Selected top players based on score.
  Enforced team constraints:
  At least one from each role
  At least one from each team
  Picked top player as Captain, second as Vice-Captain.

Output: Saved the final team to CricTensors_Output.csv.

