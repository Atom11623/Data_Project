# NBA Predictions Project

## Introduction

The NBA Predictions project aims to develop a model to predict the teams that will qualify for the 2022-2023 NBA PLAYOFFS from both the East and West conferences, as well as the eventual winners of each conference and the NBA finals. Additionally, a fictional team of 15 players will be created and its outcome for the 2022-2023 NBA season will be predicted.

## Data Sources

### Raptor Team Data
- **Total Entries**: 7289
- **Data Columns**: 23
- **Key Columns**:
  - player_name
  - player_id
  - season
  - team
  - raptor_box_offense
  - raptor_box_defense
  - raptor_box_total
  - raptor_offense
  - raptor_defense
  - raptor_total

### NBA History Data
- **Total Entries**: 28179
- **Data Columns**: 42
- **Key Columns**:
  - player_id
  - name_common
  - year_id
  - team_id
  - G
  - Min
  - MPG
  - P/36
  - TS%
  - Raptor O
  - Raptor D
  - Raptor+/-


### NBA Elo Information
- **Total Entries**: 126314
- **Data Columns**: 23
- **Key Columns**:
  - gameorder
  - game_id
  - year_id
  - team_id
  - opp_id
  - game_result

## Approach and Models

1. Data Preprocessing:
   - Handling missing values
   - Selecting relevant features
   - Merging datasets

2. Model Selection:
   - Random Forest Regression
   - Linear Regression
   - K-Nearest Neighbors Regression
   - Decision Tree Regression

3. Model Evaluation:
   - Mean Absolute Error (MAE)
   - Mean Squared Error (MSE)
   - R-squared (R2) Score

4. Model Results:
   - Decision Tree Regression outperformed other models with an R2 score of approximately 0.9997.

## Conclusion

The Decision Tree Regression model, leveraging features such as RAPTOR, WAR, and other performance metrics, proved to be highly effective in predicting NBA playoff qualification. This project demonstrates the potential of machine learning in forecasting sports outcomes.