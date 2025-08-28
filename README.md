# Project 1 📊 Cohort Analysis in Google Sheets by Tetiana Trotska
## 🔗 Project Link
📄 [Google Sheets – Cohort Analysis](https://docs.google.com/spreadsheets/d/1-U1a15GskDTBT9JHpJTTCB34thEOS4lSMbd-NBBMYrg/edit?usp=sharing)

This project demonstrates how to prepare data, build cohort analysis, and visualize user activity trends using **Google Sheets**.

---

## 🔹 Project Description
The dataset contains information about users, their activities, and engagement with different games.  
The goal was to **perform cohort analysis** to evaluate user retention and engagement across months.

---

## 🔧 Data Preparation Steps
- **Split column `game_activity_name`** into two parts:  
  - Game name  
  - Activity name  
- **Grouped 8 activity names into 5 activity types** and added them as a new column in the sheet `діяльність`.  
- In sheet `активність`:  
  - Created a column with user language (joined from `активні користувачі`)  
  - Added `Activity month number` (how many months passed since first activity month). Values are `0` or greater.  
  - Derived 3 new columns from `activity_date`:  
    - `Activity month` — the month of activity  
    - `First activity month` — user’s first month of activity  
    - `Months since first activity` — difference in months  

---

## 📈 Cohort Analysis
- Created a new sheet **`Когортний аналіз`** with a pivot table:  
  - Rows → **Activity month number**  
  - Values → **Unique users count**  
- Built a **line chart**:  
  - X-axis → Activity month number  
  - Y-axis → Number of users  
  - Added chart title and labeled axes  

---

## 🎯 Outcomes
- Clear visualization of **user retention across cohorts**  
- Insights into how many users stay active over time  
- Structured dataset for further BI/visualization tools (Looker Studio, Tableau, Power BI)

---

# Project 2. Nuclear Safety Analysis in Google Sheets by Tetiana Trotska

**Project link:**  
[Google Sheets — Nuclear Safety Analysis](https://docs.google.com/spreadsheets/d/1vkV0yPkAGKJj7JgO_6gzE1o4brZBizAkmwFKW9vRps8/edit?usp=sharing)

---

## Project Description  
Analysis of radionuclide emissions and safety indicators across Ukrainian Nuclear Power Plants (NPPs) from 2018 to 2025. Includes evaluation of stable radionuclides, cesium-137 emissions, iodine-131 emissions, composite safety index (IRG), and normalized safety index (IRG Index).

---

## Data Preparation Steps  
1. **Raw Data Collection**  
   - Original dataset imported from open source [Nuclear Safety Analysis](https://data.gov.ua/dataset/4a9d3d56-bd95-4c3e-97e7-1cdc7bcbd445) into sheet `Nuclear_safety`.

2. **Data Cleaning (`Nuclear_safety_clear`)**  
   - Renamed columns to replace `"_ "` with `"_"` (via Find & Replace).  
   - Applied **Trim whitespace** to all cells to remove invisible spaces.  
   - Converted values like `<0,01` to `0.01` using regex Find (`^\s*<\s*`) and replaced with blank, then ensured numeric format.  
   - Forced conversion to numbers by multiplying with 1 via Paste special → Multiply.  
   - Applied proper numeric formatting (2–3 decimal places).  
   - Checked non-numeric values using conditional formatting (“Text contains” / “Text is not a number”).  
   - Checked duplicates using `COUNTIFS`.  
   - Inspected outliers via a pivot table for rough anomaly checks.

3. **Data Dictionary (`Data_dictionary`)**  
   - Provided definitions and explanations of key indicators and indices.

---

## Results & Findings

###  Average Levels (`average_level_of_radionuclides`)  
- **Safest NPP:** Khmelnytskyi (KhNPP) – lowest average indices across stable radionuclides (0.01), iodine (0.01), and IRG (0.07).  
- **Least safe:** Rivne (RNPP) – highest IRG (0.20) and highest stable radionuclide index (0.06).  
- Iodine index is equally low (0.01) across all plants, suggesting no major iodine releases.

###  Cs-137 Emission Trends (`cs_137_emission`)  
- **Highest total emissions:** Zaporizhzhia (ZNPP) – 12,619 (data only until 2022).  
- **Lowest:** KhNPP – 1,535.8 total.  
- Emissions decreased at most stations; KhNPP stable, ZNPP data missing post-2022, complicating full trend analysis.

###  IRG – Composite Radiation Index (`IRG`)  
- **Highest cumulative IRG:** RNPP – 3,688.  
- **Lowest:** KhNPP – 964.  
- Level across all plants dropped from 2023–2025, but due to missing ZNPP data.

###  Normalized IRG Index (`IRG_index`)  
- **Highest:** RNPP – 5.95 total.  
- **Lowest:** KhNPP – 2.20.  
- ZNPP and PUNPP similar (~2.21 and 2.51).

###  Iodine Radionuclide Emissions (`Iodine_radionuclide`)  
- Overall low emissions and indices, indicating controlled iodine release.  
- Highest total emissions: ZNPP (4,004); Lowest: KhNPP (1,092.7).  
- No incidents detected, all stable.

###  Comparison of Radionuclide Types (`comparison_of_different_types_of_radionuclides`)  
- Long-lived radionuclides (Cs-137, stable indices) pose greater long-term threat than iodine.  
- RNPP highest in long-lived emissions (stable index 1.94, Cs-137 10,566).  
- ZNPP had highest Cs-137 until 2022 (12,619) but missing recent data.  
- KhNPP remains most environmentally safe across all metrics.

---

## Summary  
This project offers a cleaned, well-documented analysis of radionuclide emissions in Ukrainian NPPs from 2018 to 2025, with Khmelnytskyi NPP consistently appearing as the safest across multiple metrics. The structured data preparation ensures replicability.

