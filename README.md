# Exploring Simple and Main Effects of Age and Gender on Systemic Differences Using R  

This R script is designed for a comprehensive analysis of the 'Daxguard' dataset, focusing on the relationship between systemic differences (Sysdiff), age, and gender. The script starts by loading and preparing the data, converting gender into a factor for statistical processing. It performs multiple linear regression analyses: a combined analysis for both genders, and separate analyses for males and females. Additionally, it includes an ANCOVA plot to visually compare the effects of age on systemic differences by gender. The script further explores the specific effects of age and gender through a series of calculated predictions, such as the simple effects of age within males and the main effect of age across genders. This detailed analysis helps in understanding how systemic differences are influenced by age and gender in the 'Daxguard' dataset, providing valuable insights into the data's underlying patterns.  

## Basic Information
**Names:** N M Emran Hussain  
**Email:** nmemranhussain2023@gmail.com  
**Date:** January 2025  
**Model Version:** 1.0.0  
**License:** [MIT License](LICENSE)

## Intended Use
**Purpose:** The purpose of this project is to analyze the impact of age and gender on systemic differences within the Daxguard dataset, using simple and main effects models.  
**Intended Users:** Data Analysts, Data scientists, machine learning enthusiasts, educators.  
**Out-of-scope Uses:** The model is not intended for production use in any critical applications or real-time decision-making systems.

## Data Description

| **Variable Name**       | **Model Role** | **Measurement Level**  | **Description**                                            |
|-------------------------|----------------|------------------------|------------------------------------------------------------|
| Age	                    | Predictor	     | Continuous	            | Represents the age of the individual                       |
| Gender	                | Predictor	     | Categorical	          | Categorizes individuals by gender (Male, Female)           |
| Sysdiff	                | Response	     | Continuous	            | Measures the systemic differences observed in individuals  |

**Dataset Name:** Daxguard.dat  
**Number of Samples:** 400    
**Features Used:** 'Age', 'Gender'   
**Target Variable used:** 'Sysdiff'  

### Architecture  
- This model card utilizes linear model such as **'Analysis of Variance (ANOVA) & Analysis of Covariance (ANCOVA)'**.

### Evaluation Metrics  
P-value: Indicates statistical significance in multivariate level using 95% confidence level.  
b-value: Represents the magnitude and direction of 'slope' of independent variable(s)

### Version of the Modeling Software:  
- **R:** 4.3.2  
- **dplyr:** 1.1.4  

## Quantitative Analysis  

### Interpretation 
- Among males and females combined, **we cannot be reasonably certain that 'Age' is related to 'Sysdiff' because p-value is above 0.05.** Here the b-value of 'Age' indicates that 'Sysdiff' is **decreasing** with the **increase** of 'Age'.
- Among males, we can be reasonably certain that 'Age' is related to 'Sysdiff' because p-value is below 0.05. Here for males, the b-value of 'Age' indicates that 'Sysdiff' is **increasing** with the **increase** of 'Age'.
- Among females, we can be reasonably certain that 'Age' is related to 'Sysdiff' because p-value is below 0.05. Here the b-value of 'Age' indicates that 'Sysdiff' is **decreasing** with the **increase** of 'Age'.
- There's an **interaction** going on between 'Age' and 'Sysdiff' across males and females. This interaction is called **disordinal interaction** becuase **two lines are cris-crossing each other.** 
- The **simple effect** of 'Age' among **males** is **0.4594**. It means the differrence in 'Sysdiff' when we **increase** 'Age' by one unit for males thus the **expected Sysdiff** will **increase** by 0.4594 for a 1 year increase in Age for **males**.
- The **simple effect** of 'Age' among **females** is **5.28**. It means the expected Sysdiff at the average Age for females is 5.28
- The **main effect** of 'Age' is **-0.02626**. It means the average change in the predicted Sysdiff **decreases** by 0.0263 for a 1 year **increase** in age regardless of gender.
- The **main effect** of 'Gender' is 5.2556. It means at the average 'Age' level, the expected 'Sysdiff' for **females** is about **5.2556 higher** than **males**.
- The expected difference in **Sysdiff** between a **male** who is 30 years old and a **female** who is 25 years old is -25.7650.








