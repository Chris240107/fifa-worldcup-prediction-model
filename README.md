FIFA WORLD CUP PREDICTOR

A ML and Simulation based system for predicting FIFA World Cup matches and tournaments outcomes using 145+ years of international football history.

OVERVIEW

The project combines football analytics, ML, ELO ratings (as a form to describe the teams strength), and Monte Carlo simulation to estimate match outcomes and predict winners.

Instead of using historical data which can be quite inaccurate, the ELO Ratings uses a system of rating the team based on their Wins and Losses over the past few years which is more closer to reality.

FEATURES 

Historical International Football Data (1872-present)
Dynamic ELO rating system.
Team form analysis.
Match outcome prediction.
Poisson goal modeling.
Monte Carlo World Cup simulations.
Interactive prediction dashboard.
API for real-time predictions.

Dataset

Source: International Football Results Dataset

Files used:

results.csv
shootouts.csv

The dataset contains over a century of international football matches, including friendlies, qualifiers, continental tournaments, and FIFA World Cups.

Project Architecture

Raw Data
↓
Data Cleaning
↓
Feature Engineering
↓
Elo Rating Generation
↓
Machine Learning Models
↓
Match Probability Prediction
↓
Tournament Simulation
↓
Dashboard & API

Feature Engineering

The following features are generated for every match:

Elo Rating Difference
Recent Team Form
Goals Scored (rolling averages)
Goals Conceded (rolling averages)
Win Percentage
Tournament Importance
Neutral Venue Indicator
Historical Head-to-Head Statistics
Models
Elo Rating System

A dynamic rating system used to estimate team strength over time.

Match Outcome Predictor

Predicts probabilities for:

Home Win
Draw
Away Win

Algorithms explored:

Logistic Regression
Random Forest
XGBoost
LightGBM
Poisson Goal Model

Predicts expected goals for both teams and generates scoreline probabilities.

Example:

Brazil vs Germany

Expected Goals:

Brazil: 1.87
Germany: 1.32

Possible outcomes:

2-1
1-1
2-0
3-1
Tournament Simulator

The tournament engine simulates the FIFA World Cup thousands of times using predicted match probabilities.

Example output:

Team	Win Probability
Brazil	18.4%
France	16.1%
Argentina	12.7%
Evaluation Metrics

The project evaluates models using:

Log Loss

Brier Score

Accuracy

Calibration Curves

Tech Stack

Data Processing

Python

Pandas

NumPy

Machine Learning

Scikit-Learn

XGBoost

LightGBM

Visualization

Plotly

Matplotlib

Deployment

FastAPI

Streamlit

Docker

Folder Structure<br>
fifa-worldcup-predictor/<br>
│<br>
├── data/<br>
├── notebooks/<br>
├── src/<br>
├── models/<br>
├── dashboard/<br>
├── tests/<br>
└── README.md<br>

Future Improvements<br>
FIFA Rankings Integration<br>
Player-Level Features<br>
Injury and Squad Availability Tracking<br>
Betting Market Comparison<br>
Live Match Predictions<br>
Women's World Cup Support<br>
Results<br>

Current best model:

Model: XGBoost<br>
Log Loss: TBD<br>
Accuracy: TBD<br>
Brier Score: TBD<br>
Author<br>

Built as a sports analytics and machine learning project to explore football forecasting and tournament simulation.