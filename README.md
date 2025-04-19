## Members
Chee Jun Han (U2430703J) 
Leng Enjie Elston (U2430242C) 

## Life Expectancy Analysis with Machine Learning

##  Overview
This project explores the key factors influencing life expectancy across developed and developing countries. Using data via Kaggle, we implemented machine learning techniques (XGBoost and Random Forest) to uncover the most impactful predictors and propose realistic interventions to improve life expectancy globally.

## Dataset
- Source: [Kaggle Life Expectancy Dataset](https://www.kaggle.com/code/varunsaikanuri/life-expectancy-visualization/input)
- Records: 1,577
- Features: 22
- Breakdown: 1,410 developing countries | 167 developed countries


##  Data Preprocessing
- Removed unrealistic zero values in "Schooling", "Income Composition", "Under-five deaths"
- Filtered out records with populations < 20,000
- Imputed missing values with medians (by development status)
- Dropped unreliable or inconsistent features (e.g., GDP per capita, BMI, infant deaths)
- Scaled data using MinMaxScaler for modeling

## Exploratory Data Analysis
Key Correlated Features:
- **Both**: Adult Mortality, Schooling, Income Composition, Alcohol Consumption
- **Developing**: Immunisation Coverage (Polio, DTP3)
- **Developed**: Thinness (ages 5–19)

Visualization Techniques:
- Correlation heatmaps
- Boxplots, violin plots, scatter plots
- Separate analysis for developed vs developing nations

##  Modeling

### Model 1: XGBoost Regressor
- Captures complex non-linear relationships
- Revealed key features by importance
- Highlighted different impactful factors per country type

### Model 2: Random Forest Regressor
- Used to validate XGBoost findings
- Robust to overfitting and good with non-linear interactions

**Train-test split**: 75/25  
**Preprocessing**: MinMax scaling

##  Key Findings

### Common Factors
- **Adult Mortality** and **Socioeconomic Factors** are strong predictors across all countries

### Developing Countries
- Immunisation coverage significantly improves life expectancy

### Developed Countries
- Thinness in youth is a surprisingly strong predictor, potentially linked to mental health and eating disorders



##  Proposed Interventions

 Targeted Interventions to Improve Life Expectancy
Based on our analysis and model findings, we identified four key focus areas where realistic interventions can lead to an increase in life expectancy. These are detailed below:

Adult Mortality
Recommended Actions:
Increase investment in preventive healthcare, especially for individuals aged 15 to 60
Enhance support for chronic disease management to reduce premature adult deaths

Socioeconomic Factors (Schooling / Income Composition)
Recommended Actions:
Introduce education subsidies and financial support for secondary and tertiary education
Raise minimum wages to improve income composition and overall quality of life

Immunisation Coverage (Developing Countries)
Recommended Actions:
Expand access to healthcare and vaccination services, especially in rural and underserved areas
Launch targeted public health campaigns to address vaccine misinformation and increase trust

Youth Thinness (Developed Countries)
Recommended Actions:
Promote mental health awareness, particularly around body image and eating disorders
Implement school-based programs for emotional regulation, coping skills, and early intervention

##  What We Learned
- How to use **XGBoost** and **Random Forest** for regression tasks
- Feature importance analysis to drive insights
- Hyperparameter tuning for performance optimization
- Real-world interpretation of machine learning outputs


