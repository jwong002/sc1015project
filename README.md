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
     - Fix records with inconsistencies
     - Remove irrelevant columns 
     - Assess relevance of date of birth information
     - Eliminate redundant columns
     - Identify and address missing values
   - Feature Engineering:
      - Derive new features: “Spayed”, “Intact”, and gender based on existing data,
      - Categorize age into ranges,
      - Calculate length of stay based on arrival and departure dates, group durations into intervals. 
   - Data Export: Export the cleaned and enriched dataframe to a new CSV file

2. [Exploratory Data Analysis, Data-Driven Insights and Recommendations](https://github.com/jwong002/sc1015project/blob/main/Exploratory_Data_Analysis.ipynb)

   - Step 1: Exploration (Uncovering Patterns)
     - Data Checkup: Ensuring data is loaded correctly and free of errors. 
     - Understanding the Data: Analyzing the spread of data for different categories (breeds, outcomes) and numerical values (age, length of stay).
     - Outlier Patrol: Identifying potential outliers in numerical data that might skew results. 
     - Variable Connections: Exploring relationships between variables, both numerical (heatmaps) and all data types (pairwise analysis)
     - Adoption Trends: Specifically examining how adoption rates have changed over time 

   - Step 2: Feature Analysis (Uncovering Insights)
     - Age and Length of Stay: Analyzing how an animal’s age and time spent at the shelter impact adoption
     - Intake and Outcome: Exploring the relationship between how animals enter the shelter (stray, surrendered, etc;) and their final outcome (adopted, euthanized, etc;)
     - Condition and Outcome: Investigating how an animal’s health upon arrival (healthy, injured, etc;) affects their outcome
     - Multi-Variable Look: Digging deeper to see how length of stay is affected by both intake condition and outcome type

3. [Machine Learning Techniques to solve the problem](https://github.com/jwong002/sc1015project/blob/main/Machine_Learning.ipynb)
   - Data Preprocessing: 
      - Verify data types and convert them for analysis (e.g. dates to numerical format)
      - Remove rows with missing values (NaN) after conversion 
   - Exploratory Data Analysis (EDA):
      - Analyze numerical data using techniques like univariate linear regression  
   - Model Building:
      - Prepare data for machine learning models by handling both numerical and categorical features:
         - Apply general feature selection techniques
         - Train various models including:  
              - Decision Trees
              - Random Forest 
              - Lasso Regression 
              - XGBoost
                
### Conclusion
Empowering Shelters to Save More Lives

This study has shed light on several key areas where animal shelters can focus their efforts to improve adoption rates and overall animal welfare.

Prioritizing at-risk animals: Our findings suggest that shelters can achieve greater success by strategically targeting their resources towards animals with shorter stays, like strays and healthy companions.  Senior animals and those with medical conditions often face longer stays and lower adoption rates.  By devoting additional attention to these vulnerable creatures, shelters can significantly improve their well-being and increase their chances of finding loving homes.

Understanding adoption trends:  A noticeable drop in adoptions following a particularly successful year warrants further investigation.  External factors like economic shifts, social trends, and even shelter policies might be influencing people's decisions to adopt.  By delving deeper into these areas, shelters can develop comprehensive strategies to address any potential barriers to adoption.

The power of data-driven decisions:  Machine learning models like decision trees and random forests offer a powerful tool for predicting outcomes and lengths of stay.  These insights can be invaluable in identifying the factors that influence adoption rates, empowering shelters to make data-driven decisions that improve their success.

Targeted interventions:  Animals with special needs, whether behavioral or medical, can benefit tremendously from targeted intervention programs.  Shelters can partner with animal behaviorists and veterinary professionals to provide training and medical care, significantly improving the adoptability of these animals.

Tailored marketing for every pet:  Data can be a game-changer when it comes to marketing strategies.  Shelters can leverage data insights to develop targeted campaigns specifically for animals with lower adoption rates.  Raising public awareness about senior pets or those with special needs can significantly increase their chances of finding a forever home.

Continuous learning and adaptation:  The key to long-term success lies in ongoing evaluation and adaptation.  By regularly assessing the effectiveness of different models and techniques, shelters can stay ahead of the curve, refine their approaches, and continuously improve their adoption rates.

Optimizing Shelter Operations:  This study also highlights the importance of optimizing shelter operations.  Effective lost-and-found systems, detailed initial assessments, and specialized care for different intake scenarios can all contribute significantly to animal well-being and ultimately, higher adoption rates.

Resource allocation for impact:  Data-driven resource allocation allows shelters to invest strategically.  Providing additional care for animals with health challenges and prioritizing successful rehoming initiatives are just a few examples of how shelters can leverage data to maximize their impact and save more lives.

By implementing these recommendations and embracing a data-driven approach, animal shelters can create a brighter future for countless animals, ensuring they find loving homes and the happy lives they deserve.

### Key Learning Points
1. Feature Engineering (deriving new features, categorizing age into ranges, calculating length of stay)
2. Using Plotly as a tool for interactive visualization 
3. Performing ANOVA test for feature selection
4. Using 3D and 2D Scatter Plots for Actual vs Predicted Values 
5. Implementation of XGBoost, Lasso Regression, Random Forest Regressor and Cross Validation
  
### Contributors
- Jeannie Wong Yi Lin: Data Cleaning, Exploratory Data Analysis, Data Driven Insights and Recommendations, Machine Learning, Presentation Slides and Script, Video
- Jiao Yunqi: Data Cleaning, Exploratory Data Analysis, Data Driven Insights and Recommendations, Machine Learning, Presentation Slides and Script, Video
- Kwok Xin Tzi Ellis: Data Cleaning, Exploratory Data Analysis, Data Driven Insights and Recommendations, Machine Learning, Presentation Slides and Script, Video

### References
1. Data-to-Viz
2. Outliers: Keep or Drop
3. Guidelines for removing outliers
4. Regularization in Machine Learning
5. Random Forest Regression 
6. Lasso Regression
7. Introduction to XGBoost Algorithm
8. XGBoost Algorithm
9. Exploratory Data Analysis : A Beginners Guide To Perform EDA

