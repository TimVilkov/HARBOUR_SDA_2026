# HW1 — EDA + Descriptive Statistics

## Dataset download
**File:** `dataset_extended_HW1.csv`  
**Download link:** **[link](https://drive.google.com/file/d/19rEJMLiUm3AHV-KK8oOo27KbfJ7Ov2P0/view?usp=sharing)**

---

## Goal
You are given anonymized trip-level data from a bike-sharing service with two customer types:
- **casual** — pay-per-ride / day-pass users  
- **member** — annual subscribers  

Your task is to use **EDA + descriptive statistics** to propose **marketing strategies that could convert casual riders into annual members**.

This is an **EDA-only** assignment. Do not build ML models. Do not run hypothesis tests. Avoid causal claims.

---

## Dataset
**File:** `dataset_extended_HW1.csv`  
**Unit of observation:** **1 row = 1 trip**

### Columns
The dataset includes:
- trip identifiers
- bike type
- start/end timestamps
- start/end station names
- customer type (`member` vs `casual`)
- month key (`YYYY-MM`)
- station coordinates (latitude/longitude)

The dataset is intentionally not perfectly clean.

---

## Deliverables
### 1) Notebook 
A reproducible notebook that runs top-to-bottom and includes:
- data audit + cleaning decisions (with row counts before/after key filters)
- answers to the business questions below (each supported by at least one table or chart)
- a short final section with recommendations

### 2) One-page PM memo 
- 3 key findings (with references to your notebook figures/tables)
- 2 recommended actions (where + when + who + message)
- 2 limitations / risks + what data you would want next
---

## Business questions (answer all)

### 1) Demand mix and seasonality
How does usage differ between casual and member riders over time?

### 2) “When” to target casual riders
If you can show membership offers only at specific times, when should you show them?
- Explain how you would translate this into a scheduling strategy for messaging.

### 3) Trip duration: choosing the right KPI
You must choose **one primary metric** to describe “ride length” for product decision-making.
- Decide which metric you would report to a PM.
- Explain why this metric is appropriate for decision-making.

### 4) Segment differences: weekday vs weekend
How does casual behavior differ from member behavior on weekdays vs weekends?
- Provide a business interpretation of the differences you observe.

### 5) Station targeting: where to place offers
Where should you focus physical marketing (station ads) or partnerships?
- Identify high-impact stations for casual riders.
- Justify your choice.

### 6) Round trips and user intent
Round trips can reflect a different use case than one-way trips.
- Compare round-trip rates between casual and members.
- Describe what this pattern suggests about user intent and what kind of membership message would fit that intent.

### 7) Initiative design
We received user feedback suggesting that some trips are started by accident (false starts), possibly due to UI friction or docking/unlocking issues. We want to understand whether this is a meaningful problem and how we should monitor it.

Design an initiative called **“Accidental Trip Starts Investigation.”**

Your job (EDA-only):
- Propose **one or more operational definitions** for an “accidental start” using only the available trip-level data (you decide what signals to use).
- Build **a metric** that quantifies how common this issue is.
- Estimate the **scale of the issue**: what share of trips it affects and how that varies by customer type, time, bike type, and/or stations.
- Identify where the issue appears most (e.g., specific stations or time windows) and explain why that might be happening.
- Recommend **one product or operational action** to address it (e.g., UX change, station maintenance checks, user education) and specify:
  - where/when it should be applied
  - what you expect to change
- Define what “success” means for a future experiment or rollout: which metric(s) should move, and what guardrails you would track.

Notes:
- You cannot prove causality here. Treat your conclusions as descriptive and hypothesis-generating.
- Be explicit about limitations of your definition


---

## Optional (bonus): maps
Add 1–2 map visualizations:
- show how spatial usage differs between casual and members

Any hypothesis to explain it?

---

## Recommendation on visuals (brief)
Use plots when they help answer a question. Keep the total number of figures reasonable and make sure each one has a clear title and units.

---

## Grading rubric (100 points)

### 1) Data audit & cleaning decisions — 25
- timestamps parsed correctly
- missingness/duplicates/invalid values addressed transparently
- outliers handled thoughtfully (not silently removed)

### 2) Feature engineering & pandas skills — 10
- correct time features + trip type feature
- appropriate use of grouping/pivots and share/rate calculations

### 3) Descriptive statistics quality — 15
- uses robust statistics (median/IQR/percentiles) appropriately
- correct reasoning about distribution shape and outliers

### 4) Visualizations — 15
- charts match the business question and are readable
- axes, units, and sample-size awareness where relevant

### 5) Business interpretation & reasoning — 20
- conclusions are evidence-based and phrased as associations
- explanations are plausible and acknowledge alternative explanations

### 6) Initiative — 10
- segment definition is clear and measurable
- opportunity size is quantified
- success metric is defined

### 7) Communication & structure — 5
- notebook is well organized and reproducible
- PM memo is concise and actionable

### 8) Bonus — 15
- if you get more than 100 points you are allowed to allocate bonus points to any other HWs

---

## Submission
Submit:
- `HW1_<your_name>.ipynb`
- `HW1_<your_name>_PM_memo.pdf` (or markdown)

Do not include the raw dataset in your submission.

