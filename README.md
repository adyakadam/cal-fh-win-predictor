# Cal Bears Field Hockey Win Predictor

## Overview
This project uses 11 seasons of Cal Bears field hockey data (2015-2025) 
to build a machine learning model that predicts game outcomes based on 
in-game statistics. The goal is to identify the minimum stats Cal needs 
to have a high probability of winning.

## Prediction Question
Given Cal's penalty corners, shots on goal, and goalkeeper saves in a game, 
can a machine learning model predict whether Cal will win or lose and what 
thresholds of each stat make a win most likely?

## Data Collection
- Scraped game-by-game statistics from calbears.com using Selenium and BeautifulSoup
- Collected 186 games across 11 seasons (2015-2025)
- Features: penalty corners, shots on goal, goalkeeper saves
- Target: Win (1) or Loss (0)

## Key Findings
- Shots on goal is the strongest predictor of winning (correlation: 0.48)
- Cal needs 8+ shots on goal for a high win probability
- Fewer goalkeeper saves indicates less defensive pressure and correlates with wins
- Penalty corners showed minimal predictive value (correlation: 0.25)

## Models
| Model | Accuracy |
|-------|----------|
| Logistic Regression | 71% |
| Decision Tree | 61% |

## Win Probability Predictor
Built an interactive function that takes in-game stats and returns 
Cal's probability of winning, designed to help coaching staff set 
quantitative targets during games.

## Technologies
- Python
- Selenium and BeautifulSoup (web scraping)
- Pandas (data manipulation)
- Scikit-learn (machine learning)
- Matplotlib and Seaborn (visualization)

## How To Run
1. Clone the repo
2. Install dependencies: `pip install selenium beautifulsoup4 pandas scikit-learn matplotlib seaborn`
3. Run `cal_fh_probability_to_win.ipynb` in Jupyter Notebook
4. The CSV is included so you can skip the scraper and go straight to the model

## Future Work
- Add opponent stats as features
- Include home vs away as a variable
- Build a pre-game predictor based on opponent historical stats
- Expand to predict score margin instead of just win/loss