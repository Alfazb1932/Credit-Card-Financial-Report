# Credit-Card-Financial-Report
**Power BI Dashboard using MySQL Database**
**Objectibe of the Project: **
The project aims to develop a real-time credit card dashboard that provides stakeholders with actionable insights into key performance metrics and trends. It will display metrics like total revenue, income, interest earned, and customer count, segmented by demographics and usage patterns. Features include real-time data integration, detailed visualizations, predictive analytics, and automated performance alerts.
**Steps:**
**Import data to SQL database**
1.Prepare csv file
2.Create tables in SQL
3.import csv file into SQL
**Used DAX Queries:**
1) Week Num 2 = WEEKNUM( 'ccdb cc_details'[Week_Start_Date])
2) Previous_week_Reveneue = CALCULATE(
SUM('ccdb cc_details'[Revenue]),
FILTER(
ALL('ccdb cc_details'),
'ccdb cc_details'[Week Num 2] = MAX('ccdb cc_details'[Week Num 2])-1))
3) Current_week_Reveneue = CALCULATE(
SUM('ccdb cc_details'[Revenue]),
FILTER(
 ALL('ccdb cc_details'),
 'ccdb cc_details'[Week Num 2] = MAX('ccdb cc_details'[Week Num 2])))
4) wow_revenue = DIVIDE(([Current_week_Reveneue]-[Previous_week_Reveneue]),[Previous_week_Reveneue])
**Insights of this project:**
**Week 53 (31st Dec)**
W**eek Over Week Revenue Change:**
Revenue decreased by -0.99%.
Total Transaction Amount and Count increased.
Customer count increased.
Overview YTD
Overall Revenue: $57M
Total Interest: $8M
Total Transaction Amount: $46M
**Revenue by Gender:**
Male customers: $31M
Female customers: $26M
**Revenue by Card Category:**
Blue: $47M
Silver: $6M
Gold: $3M
Platinum: $1M
**State Contribution to Revenue:**
TX, NY, and CA: 68%
Activation Rate: 57.5%
Delinquent Rate: 6.06%

**Additional Insights from Dashboard**
Revenue by Week: There is a noticeable drop in revenue at the beginning of 2024, followed by a recovery.
Revenue by Age Group: The highest revenue is from the age group 30-40.
**Revenue by Income Group:**
High: $7M
Medium: $8M
Low: $10M
**Revenue by Marital Status:**
Married: $13M
Single: $11M
**Revenue by Dependent Count:**
4M: $4M
6M: $6M
7M: $7M
9M: $9M
**Revenue by Educational Level:**
Graduate: $10M
High School: $5M
Unknown: $4M
Uneducated: $4M
Post-Graduate: $2M
Doctorate: $1M
**Revenue by Expenditure Type:**
Bills: $14M
Entertainment: $10M
Fuel: $10M
Grocery: $9M
Food: $8M
Travel: $6M
**Revenue by Card Use Type:**
Swipe: $36M
Chip: $17M
Online: $4M
Revenue by Customer Job:
Businessman: $18M
White-collar: $10M
Self-employed: $9M
Govt: $8M
Blue-collar: $7M
Retirees: $5M
