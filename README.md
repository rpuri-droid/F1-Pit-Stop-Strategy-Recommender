# F1-Pit-Stop-Strategy-Recommender
Pit stop strategy is one of the most critical factors influencing success in Formula 1. The timing of stops, number of stops, tire choices, and interaction with weather and circuit layout can make the difference between winning and finishing outside the points.

Our DATA602 project aims to build a data-driven pit stop strategy recommender system. Given race conditions (driver pace, track type, weather conditions, and competitor context), the model will recommend:
- The optimal number of pit stops (1-stop vs 2-stop, etc.)
- The laps to pit on
- The tyre compound (Soft, Medium or Hard) to fit that maximizes expected finishing outcome (finish position)
- The expected performance impact (finishing position gain/loss).

This project demonstrates the full data science pipeline: data acquisition, integration, exploratory analysis, hypothesis testing, modeling, and building a practical tool for optimized decision-making.

# Datasets 
1. Formula 1 World Championship (1950 - 2024): https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020/data
  * Files we will use:
    - races.csv → Race metadata (season, circuit, date)
    - pit_stops.csv → Pit stop details (lap number, stop duration)
    - lap_times.csv → Driver performance per lap (used for stint pace and tire wear trends).
    - results.csv → Finishing positions and outcomes (measure of strategy effectiveness).
    - circuits.csv → Circuit details (track type, location).
2. Fast F1 API Dataset: https://docs.fastf1.dev/
  * We are using this to extract the following details:
    - Weather Data: Variables to extract - air temperature, track temperature, rainfall, dry/wet conditions.
    - Tyre Compound Data: Tyre compound (soft, medium, hard) per stint/lap

# Group-Members:
1. Kshitij LMU - 121507990
2. Riya Puri - 122099296
3. Stuti Patel - 122013834

