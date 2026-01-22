# Homework 3 — A/B test analysis (mobile game)

Your task is to analyze an A/B experiment in a mobile game.

Data: **[link](https://drive.google.com/drive/folders/15EUuGKaNJMxlcFVCk6jTdZstLmZLUlml?usp=sharing)]**  
Download the CSV files and put them in the same folder as the notebook.

Files:
- `history_daily.csv` — pre-period activity (daily, one row per active user-day)
- `current_daily.csv` — experiment period (daily, one row per active user-day) + `bucket` (0/1)

Notes:
- `revenue = 0` means the user was active that day but did not purchase.
- For experiment metrics we aggregate to **one row per user** over the analysis window (e.g., 28 days).

Open `HW3.ipynb` and follow the tasks in order.
