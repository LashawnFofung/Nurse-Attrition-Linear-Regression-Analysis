<h1>Data Analysis Report</h1>

<h3>Objective</h3>

To determine if a statistically significant linear relationship exists between monthly Employee Well-being Program participation rates and nurse attrition rates over three years, and to inform future retention strategies

<h3>Problem Statement</h3>
A major healthcare system faced increasing demand for nurses and persistent staffing shortages in 2025. They implemented an Employee Well-being Program to reduce job-related stress and improve nurse retention. The hospital's executive council needed to evaluate the program's efficacy to make informed decisions about future funding and expansion, especially given the substantial costs of nurse attrition.


<h3>Data & Methodology</h3>

  - <b>Independent Variable (x):</b> Program Participation Rate (%)
  - <b>Dependent Variable (y):</b> Nurse Attrition Rate (%)
  - <b>Level of Measurement:</b> Both variables are ratio variables, suitable for linear regression analysis
  - <b>Sample Size:</b> 36 observations (representing 36 months of data)
  - <b>Analysis Technique:</b> Linear Regression was chosen to quantify the relationship, enable predictive modeling, and perform statistical significance testing
  - <b>Null Hypothesis (H0):</b> There is no statistically significant linear relationship between the monthly program participation rate of nurses and the monthly nurse attrition rate

<h3>Key Findings</h3>

  - <b>R-squared:</b> The R-squared value of 0.7485 indicates that approximately 75% of the variation in the nurse attrition rate can be explained by the variation in the program participation rate. This suggests a moderate to strong fit of the model.
  - <b>Statistical Significance:</b> The p-value for the Program Participation Rate was 1.01E-11 (0.00000000001), which is less than the 0.05 significance level. This led to the rejection of the null hypothesis, concluding that the Program Participation Rate has a statistically significant effect on the Nurse Attrition Rate.
  - <b>Linear Equation:</b> The derived linear equation is: Predicted Nurse Attrition Rate =−0.081453147× Program Participation Rate + 5.268268323  This equation shows that for every 1% increase in program participation, the nurse attrition rate is predicted to decrease by approximately 0.081%.


<h3>REPORTING</h3>
This section provides a comprehensive report of the linear regression analysis. It includes the detailed output from the analysis, presenting the statistical measures and coefficients, followed by a scatter plot visualizing the relationship between the variables. Together, these elements offer a clear and complete view of the analysis results.

<h3></h3>
<b>ANALYSIS OUTPUT AND CALCULATIONS</b>
<h3></h3>


![Linear Regression](https://github.com/LashawnFofung/Nurse-Attrition-Linear-Regression-Analysis/blob/main/Results/Linear%20Regression%20Summary%20Output.png)

<h3></h3>

![Program Participation Rate Line Fit Plot](https://github.com/LashawnFofung/Nurse-Attrition-Linear-Regression-Analysis/blob/main/Program%20Participation%20Rate%20(%25)%20Line%20Fit%20Plot.png)

<h3>Implications & Recommendations</h3>

  - The program effectively reduces nurse turnover, supporting continued investment and enhancement.
  - Recommendations include enhanced promotion, barrier reduction, incentive optimization, and continuous program content improvement to increase participation.
  - The model can be used to forecast attrition rates and optimize resource allocation for recruitment and retention.
  - Limitations: The model explains 75% of the variation, meaning 25% is unexplained by other factors not included in the analysis. The analysis establishes correlation, not causation
  - Future Work: Future analyses should incorporate additional variables such as nurse job satisfaction, workload, and compensation to provide a more comprehensive understanding of attrition drivers

