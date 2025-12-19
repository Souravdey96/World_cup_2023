# World_cup_2023
📌 Project Overview

This project performs an end-to-end analytical "autopsy" of the 2023 ICC Cricket World Cup. By integrating fragmented datasets—including ball-by-ball performances, match outcomes, and player metadata—the analysis identifies the core drivers of success, from venue-specific scoring trends to the high impact of specialized playing roles.
🛠️ Tech Stack

    Language: Python

    Libraries: Pandas (Data Manipulation), Matplotlib & Seaborn (Visualization)

    Environment: Google Colab / Jupyter Notebook

🚀 Data Pipeline & Workflow
1. Data Cleaning (The Foundation)

Raw data was sanitized to ensure a "Single Source of Truth." Key actions included:

    Standardization: Resolved naming inconsistencies across datasets (e.g., matching player names).

    Type Conversion: Converted performance metrics (Runs, Wickets, Balls) from objects to integers to enable mathematical aggregation.

    Null Handling: Identified and resolved missing values in match metadata and player profiles.

2. Data Merging (The Relational Bridge)

I architected a relational model by joining four primary datasets using pd.merge:

    Enrichment: Linked individual batting and bowling rows with player roles (e.g., All-rounder, Bowler) from world_df.

    Contextualization: Connected player performances to match-level outcomes and venues from match_df.

    Validation: Confirmed a 100% success rate in merging, resulting in zero missing roles in the final analysis table.

3. Exploratory Data Analysis (Strategic Insights)

Using the "Master Table," I identified key tournament patterns:

    Venue Scoring Trends: Identified Wankhede Stadium as a high-scoring anomaly, heavily favoring teams batting first.

    Win-Type Anomalies: Discovered that India dominated the tournament primarily by defending totals (winning 9 matches by runs).

    Role Correlation: Proved that Bowlers (27.7%) and All-rounders had a higher correlation with "Player of the Match" awards than top-order batsmen alone.

📊 Key Findings (STAR Framework)

    Situation: Fragmented 2023 World Cup data across multiple CSV files.

    Task: Uncover the hidden relationship between player roles, stadium conditions, and victories.

    Action: Developed a Python pipeline to clean and merge data, followed by advanced visualization of win-type distributions and role impacts.

    Result: Validated that bowling efficiency and all-rounder versatility were the definitive differentiators in match outcomes.

🧠 Reflection & Learning

    Data Engineering: A major challenge involved manually engineering the "Player of the Match" column to bridge the gap between match results and player role profiles.

    Analytical Thinking: Learned that descriptive stats (total runs) often mask the diagnostic truth (match-winning impact).

📂 How to Run

    Clone this repository.

    Ensure the following CSVs are in the root directory: batting_df, bowling_df, match_df, world_df.

    Open the .ipynb file in Google Colab or Jupyter and run all cells.
