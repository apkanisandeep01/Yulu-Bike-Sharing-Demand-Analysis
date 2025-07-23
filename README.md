# Yulu Bike Sharing Demand Analysis

This repository contains a case study analyzing the factors influencing the demand for Yulu's shared electric cycles in the Indian market. The project involves a detailed exploratory data analysis (EDA), hypothesis testing, and provides strategic recommendations to help Yulu boost its revenues.

## 📝 Project Overview

**Yulu**, India's leading micro-mobility service provider, has experienced a dip in revenue.To address this, they've sought to understand the key factors that affect the demand for their shared electric cycles.  This project performs a comprehensive analysis of a bike-sharing dataset to identify these factors and offer data-driven recommendations.

---

## 💾 Dataset

The analysis is based on a dataset containing bike rental information over two years (2011-2012).The dataset includes 10,886 records and 12 initial columns, which were expanded with additional time-based features.

### Columns

* **datetime**: Timestamp of the rental
**season**: Season of the year (1: spring, 2: summer, 3: fall, 4: winter)
**holiday**: Whether the day is a holiday (1) or not (0) 
**workingday**: Whether the day is a working day (1) or not (0)
* **weather**:
    1: Clear, Few clouds 
    2: Mist + Cloudy 
    3: Light Snow, Light Rain 
    4: Heavy Rain, Thunderstorm
**temp**: Temperature in Celsius 
**atemp**: "Feels like" temperature in Celsius 
**humidity**: Relative humidity 
**windspeed**: Wind speed 
**casual**: Count of non-registered users
**registered**: Count of registered users 
**count**: Total number of rental bikes (casual + registered) 

---

## 🛠️ Analysis & Methodology

The project follows a structured approach to uncover insights from the data.

### 1. Data Cleaning and Preprocessing
The initial phase involved preparing the data for analysis. This included:
Converting the `datetime` column to a datetime object. 
Creating new features from the `datetime` column, such as `date`, `hour`, `day`, `month`, `year`, and `day_period`.
Mapping numerical categorical variables to their string representations for better readability (e.g., season '1' to 'spring').
Checking for and confirming the absence of null values and duplicate records. 

### 2. Exploratory Data Analysis (EDA)
EDA was performed to understand the distribution of data and the relationships between variables.
* **Univariate Analysis**: Histograms and boxplots were used to examine the distribution of numerical variables like `temp`, `humidity`, and `windspeed`. Count plots were used for categorical variables like `season`, `weather`, and `workingday`. 
**Bivariate Analysis**: Bar plots and a correlation heatmap were used to explore the relationship between different variables and the total rental count. 

### 3. Hypothesis Testing
Statistical tests were conducted to validate key hypotheses about bike rental demand.
**Working Day vs. Weekend/Holiday**: A Two-Sample Independent T-Test and a Kruskal-Wallis test were performed to check if there is a significant difference in bike demand on working days versus non-working days. 
**Impact of Weather**: ANOVA and Kruskal-Wallis tests were used to determine if weather conditions significantly affect bike rentals. 
**Impact of Season**: ANOVA and Kruskal-Wallis tests were conducted to analyze the effect of different seasons on bike demand.
**Season vs. Weather**: A Chi-square test was used to check for dependency between season and weather. 

---

## 📊 Key Findings

**Peak Demand**: The highest demand for bikes occurs in the **summer and fall** seasons, particularly in the months of **June, July, and August**. 
**Weather's Influence**: Bike rentals are highest during **clear weather** and decrease significantly with adverse conditions like rain or thunderstorms. 
**Working Days**: There is **no statistically significant difference** in the number of bike rentals between working days and non-working days. 
**Temperature and Humidity**: Higher temperatures (`temp` and `atemp`) are positively correlated with bike rentals, while higher `humidity` is negatively correlated.
**User Types**: Registered users form the bulk of the rentals and show a very strong positive correlation (0.97) with the total count. 

---

## 💡 Strategic Recommendations

Based on the analysis, the following strategies are recommended to help Yulu increase profitability:

### Optimize Operations
1.  ]**Peak Month Deployment**: Concentrate the bike fleet in high-demand areas during the peak months of June, July, and August to maximize availability and rentals. 
2.  **Weather-Responsive Deployment**: Plan bike availability based on both season and weather forecasts. For instance, ensure more bikes are available on clear days, especially during summer. 

### Marketing and Pricing
3.  **Seasonal Marketing**: Launch targeted marketing campaigns during summer to attract more users when demand is naturally high. 
4.  **Off-Peak Engagement**: Introduce promotions, discounts, or special offers during off-peak months (January-March) to stimulate demand. [c
5.  **Dynamic Pricing**: Implement a weather-responsive pricing model, potentially offering discounts during less favorable weather to encourage usage. 

### Revenue Diversification
6.  **Explore New Revenue Streams**: Diversify income by exploring partnerships, offering premium memberships, or introducing corporate sponsorships. 
