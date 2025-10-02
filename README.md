#F1 Pit Stop Strategy Recommender

Pit stop strategy is one of the most critical factors influencing success in Formula 1.  
The timing of stops, number of stops, tire choices, and interaction with weather and circuit layout can make the difference between winning and finishing outside the points.

Our **DATA602 project** aims to build a **data-driven pit stop strategy recommender system**.  
Given race conditions (driver pace, track type, weather conditions, and competitor context), the model will recommend:

- The optimal number of pit stops (1-stop vs 2-stop, etc.)  
- The laps to pit on  
- The tyre compound (Soft, Medium, or Hard) that maximizes expected finishing outcome  
- The expected performance impact (finishing position gain/loss)  

This project demonstrates the full data science pipeline: **data acquisition, integration, exploratory analysis, hypothesis testing, modeling, and building a practical tool for optimized decision-making**.

---

## Datasets 

### 1. [Formula 1 World Championship (1950 - 2024)](https://www.kaggle.com/datasets/rohanrao/formula-1-world-championship-1950-2020/data)

**Files we will use:**
- `circuits.csv` → circuit metadata (track names, locations, lengths)  
- `constructors.csv`, `constructor_results.csv`, `constructor_standings.csv` → team-level details  
- `drivers.csv`, `driver_standings.csv` → driver information and rankings  
- `lap_times.csv` → lap-by-lap timings for each driver in each race  
- `pit_stops.csv` → pit stop timings, lap numbers, durations  
- `qualifying.csv` → qualifying results and grid positions  
- `races.csv`, `seasons.csv` → race and season information  
- `results.csv`, `sprint_results.csv` → race and sprint outcomes  
- `status.csv` → finishing status (accident, engine failure, etc.)  

**Why this dataset?**
- Covers multiple seasons and circuits with consistent schemas.  
- Enables learning of generalizable patterns across **track types, eras, and regulations**.  
- Pit stop and lap time data allow us to build **stint-level performance views** and measure:
  - Lap time drift within stints  
  - Undercut/overcut windows  
  - Value of track position vs. tyre freshness  
- Tables link through stable keys (season, race, driver), making joins straightforward.  

---

### 2. [FastF1 API Dataset](https://docs.fastf1.dev/)

**Features we will extract:**
- Weather data → air/track temperature, humidity, wind speed  
- Tyre compound data → compound choice (soft, medium, hard) per stint/lap  
- Safety car information  

**Why this dataset?**
- Provides **tyre and stint data** critical for simulating strategies.  
- Captures **dynamic race conditions** (weather, safety cars) that directly influence pit decisions.  

---

## Group Members
1. **Kshitij LNU** – 121507990  
2. **Riya Puri** – 122099296  
3. **Stuti Patel** – 122013834  
