# Airbnb Listings EDA & Sentiment Analysis (Singapore)

## Project Overview
This is a group project focused on conducting a comprehensive Exploratory Data Analysis (EDA) and sentiment analysis of Airbnb listings in Singapore, using data from Inside Airbnb (https://insideairbnb.com/get-the-data/).

The goal is to uncover insights into pricing, availability, host behavior, and customer satisfaction using real-world data.

---

## Objectives
- Perform a full EDA workflow on real-world data  
- Clean and preprocess messy datasets  
- Analyze pricing, location, and property characteristics  
- Explore host behavior and listing performance  
- Conduct sentiment analysis on customer reviews  
- Generate actionable insights through visualization  

---

## Dataset
We used two datasets for Singapore:

- `listings.csv.gz` → Property, host, pricing, availability  
- `reviews.csv.gz` → Guest review text data  

Source: Inside Airbnb  
Data dictionary: https://docs.google.com/spreadsheets/d/1iWCNJcSutYqpULSQHlNyGInUvHg2BoUGoNRIGa6Szc4  

---

## Tech Stack
- Python  
- Pandas, NumPy  
- Plotly  
- Matplotlib / Seaborn  
- NLTK / TextBlob (for sentiment analysis)  
- Jupyter Notebook  

---

## Project Workflow

### 1. Data Loading & Setup
- Imported datasets and inspected structure  
- Reviewed data types and memory usage  

### 2. Data Cleaning & Preprocessing
- Converted:
  - `price` → numeric  
  - percentage columns → numeric  
  - date columns → datetime  
  - boolean columns → True/False  
- Handled missing values  
- Identified and treated outliers  

### 3. Exploratory Data Analysis
- Univariate analysis (distributions)  
- Bivariate analysis (relationships)  
- Geographic analysis by neighborhood  
- Host behavior analysis  

### 4. Visualization
- Interactive plots using Plotly  
- Focus on pricing, location, and listing characteristics  

### 5. Sentiment Analysis
- Processed review text data  
- Calculated sentiment polarity  
- Linked sentiment to ratings, pricing, and host metrics  

---

## Key Insights
- Most listings accommodate 2–3 guests  
- Prices vary significantly by location and property type  
- Many listings have low review counts  
- Review scores are generally high (approximately 4.5/5)  
- Some extreme outliers exist in availability and stay limits  
- Superhosts and responsive hosts tend to perform better  

---

## Data Challenges
- Incorrect data types (prices, percentages)  
- Missing values in review-related columns  
- Skewed distributions  
- Extreme outliers (e.g., maximum nights)  

---

## Business Implications
- Optimize pricing based on location and listing type  
- Improve performance of low-review listings  
- Use sentiment insights to enhance guest experience  
- Identify demand patterns through availability analysis  

---