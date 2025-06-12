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

<h3>ANALYSIS TECHNIQUE JUSTIFICATION</h3>
Given the hospital's objective to mitigate nurse attrition through the Employee Well-being Program, and the need to determine if a significant linear relationship exists between monthly program participation and nurse attrition rates over the past three years, linear regression was selected as the appropriate analytical technique. This choice is supported by several key factors:
  
  - Quantifying the Relationship: Linear regression allows for the precise quantification of the relationship between program       participation rates (independent variable) and nurse attrition rates (dependent variable). It determines the strength and direction of this relationship, providing insights into how changes in participation rates influence attrition. This directly addresses the core question of whether a statistically significant relationship exists.
  - Predictive Modeling: Should a statistically significant relationship be established, linear regression generates a predictive linear equation. This equation can then be utilized to forecast future nurse attrition rates based on varying program participation rates. This capability is essential for strategic planning and resource allocation, enabling the hospital to make informed decisions regarding program adjustments and retention strategies.
  - Statistical Significance Testing: Linear regression provides a framework for testing the null hypothesis, which states that no statistically significant linear relationship exists between monthly program participation rates and nurse attrition rates. By calculating the p-value, we can determine the likelihood that any observed relationship is a genuine effect of the program rather than a result of random variation. This is crucial for evaluating the program's efficacy, as outlined in the business scenario.

In summary, linear regression is a critical analytical tool for this context. It allows for the examination and quantification of the relationship between program participation and nurse attrition, facilitating an assessment of the program's effectiveness. Moreover, the predictive capabilities of linear regression enable the hospital to make data-driven decisions regarding resource allocation and program enhancements. Finally, the statistical significance testing provides a rigorous evaluation of the program's impact, ensuring that any conclusions drawn are statistically sound.

<h3>LINEAR REGRESSION ANALYSIS</h3>
The following section presents the methodology and results of the linear regression analysis used to investigate the relationship between the monthly program participation rate and the monthly nurse attrition rate. This section includes a description of the data, the statistical output from the regression analysis, and a visual representation of the data, providing a comprehensive overview of the analytical process.

<h3>DESCRIPTION OF RELEVANT DATA</h3>
The linear regression analysis utilizes a dataset with specific characteristics, which are important for proper interpretation of the results; these characteristics, including the independent and dependent variables, their levels of measurement, and the sample size, are outlined in the following description.

<h3></h3>

<b>Data Characteristics</b>

  - The independent variable (x) in this analysis is the Program Participation Rate (%), representing the percentage of nurses involved in the Employee Well-being Program. This variable is used to predict or explain variations in the dependent variable.
  - The dependent variable (y) in this analysis is the Nurse Attrition Rate (%), which indicates the percentage of nurses who left their employment during each month. The analysis aims to model how this attrition rate is influenced by changes in the program participation rate.
  - The level of measurement for both the Program Participation Rate and the Nurse Attrition Rate are ratio variables. This means they are quantitative, have a true zero point (indicating the absence of the measured quantity), and allow for meaningful ratio comparisons (e.g., a rate of 20% is twice as high as a rate of 10%). The ratio level of measurement is essential for linear regression, as it assumes a linear relationship between the quantitative variables.
  - The sample size for this analysis is 36 observations, representing data collected across 36 months. Each observation consists of a paired value of Program Participation Rate and Nurse Attrition Rate for a specific month. The sample size of 36 is sufficient to perform a linear regression analysis and provides a reasonable amount of data to assess the relationship between the variables over time.

<h3>REPORTING</h3>
This section provides a comprehensive report of the linear regression analysis. It includes the detailed output from the analysis, presenting the statistical measures and coefficients, followed by a scatter plot visualizing the relationship between the variables. Together, these elements offer a clear and complete view of the analysis results.

<h3></h3>
<b>ANALYSIS OUTPUT AND CALCULATIONS</b>
<h3></h3>


![Linear Regression](https://github.com/LashawnFofung/Nurse-Attrition-Linear-Regression-Analysis/blob/main/Linear%20Regression%20Summary%20Output.png)

<h3></h3>

![Program Participation Rate Line Fit Plot](https://github.com/LashawnFofung/Nurse-Attrition-Linear-Regression-Analysis/blob/main/Program%20Participation%20Rate%20(%25)%20Line%20Fit%20Plot.png)

<h3></h3>

<h3>IMPLICATIONS OF DATA ANALYSIS</h3>
This section provides a comprehensive interpretation of the linear regression analysis results. It begins by evaluating the model's overall fit using R-squared and assessing the statistical significance of the program participation rate's influence on nurse attrition. Subsequently, the practical application of the generated linear equation for predictive modeling will be examined. Following this, the limitations of the analysis are discussed, and finally, a recommended course of action, based on the analytical findings and relevant business context, is presented to guide the hospital's strategic management decisions regarding the Employee Well-being Program.

<h3></h3>

<h3>GOODNESS OF FIT</h3>h
The goodness of fit of the linear regression model describes how well the model represents the observed data. A key statistic for assessing this in linear regression is the coefficient of determination, or R-squared (R2). The R-squared value is presented as a percentage, ranging from 0% to 100%, to provide a readily understandable measure of the model's explanatory power.

In the regression output, the R-squared value is 0.7485. This indicates that approximately 75 % of the variation in the nurse attrition rate can be explained by the variation in the program participation rate.

<h3></h3>

<b>Interpretation:</b>
  
  - An R-squared of 0% indicates a weak fit, meaning the model explains none of the variability of the dependent variable.
  - An R-squared of 50% indicates a moderate fit, meaning the model explains some of the variability.
  - An R-squared of 100% indicates a strong fit, meaning the model perfectly explains all the variability.

Therefore, an R-squared of 0.7485 indicates a moderate to strong fit of the variability in nurse attrition, but there's still a considerable amount of variation not accounted for by the model. Therefore, program participation accounts for 75 % of variation in nurse attrition. This leaves 25% of the variation was not measured in this analysis. This implies that while program participation rate is a relevant factor in explaining nurse attrition, other factors not included in this analysis also play a significant role.

<h3></h3>


<h3>INDEPENDENT VARIABLE(S) SIGNIFICANCE</h3>

In linear regression, assessing the significance of the independent variable(s) is crucial to determine if they have a statistically meaningful impact on the dependent variable. Statistical significance indicates whether the observed effect is likely a real effect or simply due to random chance. Statistical significance was assessed at the 0.05 level (indicating a 95% confidence level) and 0.95 level (indicating a 5% significance level).

For this analysis, the independent variable is the Program Participation Rate. The significance of this variable is evaluated using its p-value from the regression output. The p-value is a measure of how 'unsure' we are about the Program Participation Rate. The aim is to have a low p-value. A high p-value means we are more 'unsure' (i.e., the results could easily be due to chance), while a low p-value means we are less 'unsure' and more confident in the effect the Program Participation Rate has on Nurse Attrition.

From the output, the p-value for the Program Participation Rate is 1E-11 (or 0.00000000001), representing a probability of less than 1%. Therefore, we reject the null hypothesis and conclude that the Program Participation Rate has a statistically significant effect on the Nurse Attrition Rate. This suggests that changes in program participation strongly predict changes in nurse attrition and this association is unlikely to be due to random chance.

