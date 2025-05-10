# 📊 Blinkit Marketing Performance Analysis 

A comprehensive data analysis project to track and optimize Blinkit's marketing campaigns using ad spending, and conversion metrics.

![Logo](https://upload.wikimedia.org/wikipedia/commons/thumb/2/2f/Blinkit-yellow-app-icon.svg/250px-Blinkit-yellow-app-icon.svg.png)

<br>

## 🧠 About the Project

This project analyzes Blinkit's marketing performance by exploring how various marketing channels and campaigns impact user engagement and conversions. It helps identify which channels deliver the best returns and where improvements can be made.

<br>

## 🎯 Project Objectives

- Build a concise and insightful dashboard to track the performance of all marketing campaigns and channels.
- Answer key business questions such as:
  - Which marketing channels are contributing the most to customer acquisition?
  - What is the ROI of each channel, and where should we reallocate budget for maximum impact?
  - Are there specific time periods (e.g., days or festivals) when revenue generated through marketing channels has a higher impact?


<br>

## 📁 Dataset Information

- **Source**: Kaggle
- **File**: `blinkit_marketing_performance.csv`
- [📄 View the Dataset](Blinkit_Marketing_Performance.csv)


<br>

## 🛠️ Tools & Technologies Used

- **Language**: SQL (MySQL)
- **Visualization**: Power BI
- **IDE**: MySQL Workbench
- **Others**: SQLAlchemy (Python for exporting data)


<br>

## 🧹 Data Preprocessing

- Explored the dataset using MySQL and prepared it for further analysis.
- Checked for missing values and modified the date column's data type from text to date,ensuring standardization in data.
- Calculated new metrics such as ROAS (Return on Ad Spend).
- Exported the processed dataset to a CSV file using a Python script with SQLAlchemy.
  
- [🗂️ View Python File](query_to_csv.py)

- [🗂️ View full SQL Query File](BLINKIT_MARKETING_PERFORMANCE_SQL.sql)
  
- SQL code snippet
```sql
SELECT count(*) FROM marketing_performance;

-- CHECKING THE DATA TYPE OF THE DATE COLUMN

DESCRIBE marketing_performance;

-- CONVERTING THE DATA TYPE OF DATE COLUMN FROM TEXT TO DATE

ALTER TABLE marketing_performance
 MODIFY COLUMN date DATE;


SELECT column_name, data_type
FROM information_schema.columns
WHERE table_name = 'marketing_performance';
```


<br>

## 📊 Exploratory Data Analysis (EDA)

- Loaded the CSV into Power BI for visualization.
- Calculated key marketing metrics including CTR (Click-Through Rate), Cost per Conversion, ROAS, and Conversion Rate.
- Analyzed spend vs. revenue, monthly revenue trends by channel, and conversions by channel.


<br>


## 📈 Visualizations

- Designed a **number-focused dashboard** in Power BI to highlight business-relevant metrics.
- Included KPI cards to display key values like total conversions, revenue, and ad spend.
- Created bar charts showing monthly revenue, total conversions, and spend-to-revenue ratios across various channels.
- Added a table to highlight the **top 5 performing campaigns** based on conversion rates.

- [📊 Download Power BI Dashboard (pbix)](Blinkit_Marketing_Dashboard.pbix)     [📊 Dashboard Image](Dashboard_Image.png)

<p align="center">
  <img src="Dashboard_Image.png" alt="Power BI Dashboard" width="500">
</p>


<br>

## 🔍 Key Insights & Conclusions

- Although all channels performed relatively well, campaigns run via the **official app** achieved the **highest conversion rates**.
- **Email campaigns** delivered the highest revenue relative to spend, indicating strong ROI and suggesting increased priority during budget planning.
- **Revenue peaked between April and October**, despite consistent ad spend, hinting at seasonal effects or event-driven spikes.


<br>

## 📝 Recommendations

- Reallocate a portion of marketing spend from **SMS** to **email** and **in-app** campaigns to boost overall conversions.
- Prioritize email campaigns during peak seasons based on ROI patterns.
- Continuously optimize campaign content to engage and attract new audiences.


