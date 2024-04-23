# SC1015 Mini Project - Optimizing Shelter Management and Boosting Adoption Rates
## About

This is the mini project for SC1015 - Introduction to Data Science and Artificial Intelligence (DSAI). We performed analysis on the animal shelter  [dataset](https://data.austintexas.gov/Health-and-Community-Services/Austin-Animal-Center-Outcomes/9t4d-g238/about_data) from the open data portal of the City of Austin, Texas.  

### Members
- Jeannie Wong Yi Lin 
- Jiao Yunqi
- Kwok Xin Tzi Ellis

### Problem Motivation
Data-driven initiatives are vital for improving animal shelter operations, reducing overcrowding, and raising adoption rates. Shelters can use historical and real-time data to identify relevant characteristics, predict adoption results, and modify their resources and care procedures accordingly. Machine learning models provide predicted insights, helping shelters prioritize animals and improve their adoption processes. Continuous monitoring and modification to feedback guarantee that shelters can successfully adjust to changing circumstances, resulting in improved animal care and more efficient shelter management. 

### Problem Definition 
How do we optimize the management of animal shelters and increase adoption rates? 

### Resources (found in this folder) 
- [Original Dataset (intakes)](https://github.com/jwong002/sc1015project/blob/main/Austin_Animal_Center_Intakes_20240327.csv)
- [Original Dataset (outcomes)](https://github.com/jwong002/sc1015project/blob/main/Austin_Animal_Center_Outcomes_20240327.csv)
- [Cleaned and Merged Dataset](https://github.com/jwong002/sc1015project/blob/main/train_cleaned.csv)
- Presentation Slides (insert link)
- Video can be assessed from this link (insert link)

### Walk-Through

1. [Data Preparation and Cleaning](https://github.com/jwong002/sc1015project/blob/main/Data_Preparation_Cleaning.ipynb)
   
   - Data Merging: Combine intakes and outcomes datasets into a single one.
   - Data Cleaning: 
            Fix records with inconsistencies,
            remove irrelevant columns, 
            assess relevance of date of birth information,
            eliminate redundant columns,
            identify and address missing values
   - Feature Engineering:
            Derive new features: “Spayed”, “Intact”, and gender based on existing data,
            categorize age into ranges,
            calculate length of stay based on arrival and departure dates, group durations into intervals. 
   - Data Export: Export the cleaned and enriched dataframe to a new CSV file

2. [Exploratory Data Analysis, Data-Driven Insights and Recommendations](https://github.com/jwong002/sc1015project/blob/main/Exploratory_Data_Analysis.ipynb)

   Step 1: Exploration (Uncovering Patterns)
   - Data Checkup: Ensuring data is loaded correctly and free of errors. 
   - Understanding the Data: Analyzing the spread of data for different categories (breeds, outcomes) and numerical values (age, length of stay).
   - Outlier Patrol: Identifying potential outliers in numerical data that might skew results. 
   - Variable Connections: Exploring relationships between variables, both numerical (heatmaps) and all data types (pairwise analysis)
   - Adoption Trends: Specifically examining how adoption rates have changed over time 

   Step 2: Feature Analysis (Uncovering Insights)
   - Age and Length of Stay: Analyzing how an animal’s age and time spent at the shelter impact adoption
   - Intake and Outcome: Exploring the relationship between how animals enter the shelter (stray, surrendered, etc;) and their final outcome (adopted, euthanized, etc;)
   - Condition and Outcome: Investigating how an animal’s health upon arrival (healthy, injured, etc;) affects their outcome
   - Multi-Variable Look: Digging deeper to see how length of stay is affected by both intake condition and outcome type

3. Machine Learning Techniques to solve the problem
   - Data Preprocessing: 
   Verify data types and convert them for analysis (e.g. dates to numerical format),
   remove rows with missing values (NaN) after conversion 
   - Exploratory Data Analysis (EDA):
   Analyze numerical data using techniques like univariate linear regression  
   - Model Building:
                              -    Prepare data for machine learning models by handling both numerical 
                                   and categorical features:
                             -     Apply general feature selection techniques
                             -     Train various models including:  
                                    a) Decision Trees
                                    b) Random Forest 
                                    c) Lasso Regression 
                                    d) XGBoost 

 
