# Health, Nutrition & Lifestyle Management System

**Data Integration & Warehousing Project**
Integrated Analysis of Lifestyle, Nutrition, and Physical Activity

## Overview
This project combines health, nutrition, sleep, and physical activity data from multiple sources into one unified data warehouse. It analyzes the relationships between nutrition, sleep quality, stress levels, and physical activity.

## Team
| Name | ID |
|---|---|
| Lamar Abdel Aziz Alqurashi
| Jana Abdul Rauf Saati 
| Fatima Shaker Alharthi 

## Data Sources
| Dataset | Type | Description |
|---|---|---|
| Sleep Health & Lifestyle | Structured | Sleep quality, duration, stress, demographics |
| Daily Food & Nutrition | Structured | Meals, calories, protein, fats, carbohydrates |
| Fitbit Daily Activity (dailyActivity_merged) | Structured | Steps, distance, calories, activity minutes |
| Food Reviews | Unstructured | User review text and ratings (sentiment analysis) |

## Project Workflow
1. **Scenario & Data Sources:** profiling the four datasets.
2. **Structured vs. Unstructured Data:** classification of each source.
3. **Data Cleaning & Preprocessing:** duplicates, outliers (IQR), missing values, data types, blood pressure split, text preprocessing and sentiment analysis.
4. **Schema Matching:** identifying equivalent attributes across sources.
5. **Schema Mapping:** mapping rules written in SQL style.
6. **Star Schema, Data Warehouse & ETL:** design and loading.
7. **Strategic Questions + OLAP:** SQL queries answering business questions.
8. **Visual Dashboards:** charts of the key insights.

## Star Schema
- **Fact table:** `FACT_HEALTH_ACTIVITY` (DailySteps, PhysicalActivityLevel, SleepDuration, StressLevel, Calories, SentimentScore)
- **Dimensions:**
  - `DIM_PERSON` (Gender, Age, Occupation, BMI_Category)
  - `DIM_FOOD` (Meal_Type, Food_Item, Category)
  - `DIM_REVIEW` (ProductID, Rating, Helpfulness_Score, Sentiment_Label)

## ETL Process
- **Extract:** from the Fitbit, Sleep Health, Food Nutrition, and Food Reviews datasets.
- **Transform:** cleaning, type conversion, schema matching/mapping, and converting review text into sentiment features.
- **Load:** into the star schema in MySQL (50 rows per table).

## Business Questions
1. Which meal type has the highest average calories?
2. How do stress levels and sleep duration vary across BMI categories?
3. Which meal type receives the most positive reviews?
4. Which occupation has the highest total calories and daily steps?

## Repository Structure
```
/docs   → presentation and lab reports
/code   → Python (cleaning, sentiment) and SQL scripts
/data   → datasets (if allowed)
README.md
```

## Tools
Python (pandas), MySQL, Google Sheets (charts)

## Final Recommendations
- Encourage healthier nutrition and sleep habits.
- Expand the warehouse with additional healthcare datasets.
- Apply machine learning models for future health prediction.
