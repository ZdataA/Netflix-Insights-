## Netflix User Analysis Dashboard

**Project Overview**  

This project analyzes a Netflix Users Dataset from Kaggle, focusing on user behavior, subscription types, and viewing patterns.
 The goal is to understand subscription trends, watch time distribution, and audience demographics, and to uncover actionable insights that Netflix (or any streaming platform) could use to improve engagement and revenue.
Dataset: Netflix Users Dataset (Kaggle)

**Business Problem**

Streaming platforms face constant challenges:

 - Which subscription tier contributes the most to engagement?


 - What content genres keep users most entertained?


 - Which countries bring the highest user base?


 - How can Netflix improve retention by leveraging user insights?


**Steps Taken:**
1. **Data Cleaning:**  
   - Removed blanks & duplicates.  
   - Standardized countries and subscription values.
   - Fixed inconsistent genre entries.

2. **Excel Analysis (Pivot Tables & Charts)**  
   - Users by subscription type.
   - Watch time by subsciption type.
   - Popular genres.
   - Users by country.

3. **SQL Analysis**  
    To simulate real-world business questions, I wrote SQL queries:  
     ```sql
     -- 1. Count users by subscription type
     SELECT Subscription_Type, COUNT(User_ID) AS Total_Users
     FROM Netflix_Users
     GROUP BY Subscription_Type;
     ```

    ```sql
    -- 2. Average watch time per subscription
    SELECT Subscription_Type, AVG(Watch_Time_Hours) AS Avg_Watch_Time
    FROM Netflix_Users
    GROUP BY Subscription_Type;
    ```

    ```sql
    -- 3. Top 5 countries by user count
    SELECT Country, COUNT(User_ID) AS User_Count
    FROM Netflix_Users
    GROUP BY Country
    ORDER BY User_Count DESC
    LIMIT 5;
    ```

   ```sql
   -- 4. Most popular genre overall
   SELECT Genre, COUNT(User_ID) AS Genre_Count
   FROM Netflix_Users
   GROUP BY Genre
   ORDER BY Genre_Count DESC
   LIMIT 1;
   ```

4. **Tableau Dashboard**

 Created a Tableau dashboard with:
   - Bar chart: Users by Subscription Type
   - Bar chart: Genre popularity 
   - KPI Cards: Percent of Premium Users, Total Users, Avg. Watch Time




**Key Insights**
- **Premium is Dominant**: Highest users & watch time  
- **Content Drives Engagement**: Horror is the most popular genre  
- **Geographic Distribution**: UK leads user count, followed by Germany & India
- **Retention Opportunity**: Standard users watch less → higher churn risk

**Business Recommendations**
- Upsell Standard to Premium with discounts & bundled offers.
- Invest in Horror & Documentary content, since they drive engagement.
- Expand marketing in the UK, Germany, India, where Netflix has a strong base.
- Churn Management: Encourage Standard users with personalized nudges.

**Files:**
- `netflix_users.xlsx`: Cleaned data + pivot tables
- `Netflix Project.png`: Excel dashboard visualization  
- `sql_queries.sql`: SQL for all analysis  
- `tableau_dashboard.twbx`: Tableau dashboard 
- `README.md`: Full project documentation

**Why This Project Matters**

This project demonstrates end-to-end data analysis workflow:
  - Data Cleaning (Excel)
  - KPI Reporting (Pivot Tables & Charts)
  - Querying & Aggregation (SQL)
  - Dashboarding (Tableau)
  - Business Insights & Recommendations

It shows technical ability + business impact → exactly what employers look for in a Data Analyst.


## 🌐 Connect with Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-zaher--ahmed-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/zaher-ahmed-777506199/)

---

<!--
**ZdataA/ZdataA** is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
-->
