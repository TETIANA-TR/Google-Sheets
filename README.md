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

