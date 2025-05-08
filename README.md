# Google-Sheets
Getting to know Google Sheets
1. On the “activity” sheet, I split the game_activity_name column into two parts: the game name and the activity name.
2. I combined the 8 activity names into 5 activity types, and displayed the activity type in the “activity” sheet as a separate column.
3. In the “activity” sheet, I created a column with the user’s language and filled it in using data from the “active users” sheet.
Activity month number — the number of the activity month. That is, how many months have passed from First activity month to Activity month. The values ​​in this column can only be 0 or greater than zero.
4. In the activity sheet, I created three columns that are derived from the activity_date column:
Activity month — the month of activity, that is, the month in which activity_date is included.
First activity month — the first month of activity for each user.
5. Created a new sheet “Cohort analysis” with a pivot table that uses data from the sheet “activity”.
6. In the pivot table, displayed the Activity month number in the rows and the number of unique users as the value.
7. Visualized the number of users in each month of activity. Created a line chart with the horizontal axis — Activity month number and the vertical — the number of users who have the corresponding month number.
8. Filled in the title of the chart and its axes.
