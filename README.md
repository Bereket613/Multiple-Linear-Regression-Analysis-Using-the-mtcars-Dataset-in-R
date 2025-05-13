# Multiple-Linear-Regression-Analysis-Using-the-mtcars-Dataset-in-R

## Group Members
- Natnael Bekele (DBU1501407)
- Hafiz Hussen (DBU1501241)
- Rediet Esubalew (DBU1501704)
- Bereket Getaw (DBU1501044)
- Dawit Alemu (DBU1501117)
- Yiferu Mekonen (DBU1501562)
- Elbetel Abedi (DBU1501145)
- Genet Minda (DBU1501217)

## Overview
This project uses the `mtcars` dataset in R to build and analyze a multiple linear regression model predicting `mpg` (miles per gallon) based on several automobile features: 
- `hp` (horsepower)  
- `wt` (weight)  
- `qsec` (1/4 mile time)  
- `cyl` (cylinders)  
- `disp` (displacement)

## Steps Performed
![image](https://github.com/user-attachments/assets/8f9fcd30-3d1e-4aeb-8e19-e07872b8da20)

### 1. Initial Model Fitting
- Fitted `mpg ~ hp + wt + qsec + cyl + disp`
- Assessed model summary, coefficients, residuals, R-squared, and significance of predictors.
- ![image](https://github.com/user-attachments/assets/b7c97ebb-ea30-437e-941a-f1920058bd3e)


### 2. Assumption Checks
- **Linearity:** Assessed using Residuals vs Fitted plot.
- **Homoscedasticity:** Checked using Goldfeld-Quandt test.
- **Normality of Residuals:** Tested using Shapiro-Wilk test.
- **Multicollinearity:** Evaluated using Variance Inflation Factor (VIF).
![image](https://github.com/user-attachments/assets/f5fcafae-32e7-4b12-a04b-ae048ef2a03e)

### 3. Remedial Measures
- Centered variables (`hp` and `wt`) to reduce multicollinearity.
- Dropped highly correlated predictors (`cyl`, `disp`).
- Added interaction term (`hp_centered * wt_centered`) to capture non-linear relationships.
![image](https://github.com/user-attachments/assets/e0097eea-f224-4bc5-9102-37e1101ad594)

### 4. Refitting Improved Model
- New model: `mpg ~ hp_centered + wt_centered + hp_centered:wt_centered + qsec`
- Reassessed all assumptions with updated diagnostics.
- Compared performance metrics: Residual Standard Error, R-squared, Adjusted R-squared.

## Results
- The improved model explains ~89% of the variance in `mpg`.
- All assumptions (linearity, homoscedasticity, normality, low multicollinearity) are better satisfied.
- The interaction term significantly enhances interpretability.
- ![image](https://github.com/user-attachments/assets/3143db1e-0ff4-48f6-a093-8ab1bcd8447f)


## Tools Used
- **R Programming Language**
- **R Packages:** `car`, `lmtest`, `nlme`

## Conclusion
Through model diagnostics and refinements, the project demonstrates the practical application of regression analysis and assumption testing, resulting in a more reliable and interpretable predictive model.
