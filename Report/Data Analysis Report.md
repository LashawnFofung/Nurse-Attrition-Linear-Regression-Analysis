# Nurse Attrition Analysis Report
### Linear regression of well-being program participation and nurse attrition

**Prepared by:** Lashawn Fofung · **Course:** Data-Driven Decision Making (MBA, WGU) · **Tool:** Excel Analysis ToolPak

[← Back to project overview](../README.md) · [🎥 Presentation](https://youtu.be/mEK-_1xrKpA)

---

## Contents
1. [Executive Summary](#1-executive-summary)
2. [Problem Statement](#2-problem-statement)
3. [Objective & Hypotheses](#3-objective--hypotheses)
4. [Data](#4-data)
5. [Methodology](#5-methodology)
6. [Results](#6-results)
7. [Model Diagnostics](#7-model-diagnostics)
8. [Interpretation](#8-interpretation)
9. [Limitations](#9-limitations)
10. [Recommendations](#10-recommendations)
11. [Conclusion](#11-conclusion)

---

## 1. Executive Summary

Over 36 months, **higher participation in the Employee Well-being Program was strongly associated with lower nurse attrition.**

- Participation explains **74.8%** of the month-to-month variation in attrition (R² = 0.748).
- The relationship is highly significant (p = 1.01 × 10⁻¹¹).
- Each **10-percentage-point** increase in participation is associated with about **0.81 points lower** monthly attrition.
- From year 1 to year 3, average participation rose from **15.4% to 39.9%**, while average attrition fell from **4.17% to 2.18%**.

**Recommendation:** continue funding the program, work to raise participation, and add better measurement to confirm the program itself is driving the improvement.

---

## 2. Problem Statement

A major healthcare system faces rising demand for nurses and persistent staffing shortages. Three years ago, it launched an **Employee Well-being Program** to reduce job-related stress and improve retention.

Nurse attrition is costly: each departure brings recruiting, onboarding, and overtime costs, and can strain patient care. The hospital's executive council needs to know whether the program is working before deciding on future funding and expansion.

---

## 3. Objective & Hypotheses

**Objective:** determine whether a statistically significant linear relationship exists between monthly program participation and monthly nurse attrition, and use the result to guide retention strategy.

| | |
|---|---|
| **Null hypothesis (H₀)** | There is no linear relationship between participation rate and attrition rate (slope = 0). |
| **Alternative hypothesis (H₁)** | There is a linear relationship between participation rate and attrition rate (slope ≠ 0). |
| **Significance level (α)** | 0.05 |

---

## 4. Data

- **Source:** monthly program data provided by Western Governors University for this course (may be simulated)
- **Sample:** 36 consecutive months
- **File:** [Nurse Attrition and Participation Program Data.xlsm](../Data/Nurse%20Attrition%20and%20Participation%20Program%20Data.xlsm)

| Variable | Role | Type | Range | Mean |
|---|---|---|---|---|
| **Program participation rate (%)** | Independent (x) | Ratio | 9.3% – 44.3% | 27.7% |
| **Nurse attrition rate (%)** | Dependent (y) | Ratio | 1.4% – 5.0% | 3.01% |

**Trend by year**

| | Year 1 | Year 2 | Year 3 |
|---|---|---|---|
| Average participation | 15.4% | 27.8% | 39.9% |
| Average attrition | 4.17% | 2.68% | 2.18% |

---

## 5. Methodology

**Why linear regression?**
- Both variables are numeric (ratio level), and the question is how one changes as the other changes.
- A scatter plot shows a roughly straight-line, downward pattern.
- Regression provides a significance test, a measure of fit (R²), and an equation for prediction.

**Steps**
1. Plot participation (x) against attrition (y) to check for a linear pattern.
2. Run a simple linear regression with the Excel Analysis ToolPak.
3. Test H₀ using the slope's p-value at α = 0.05.
4. Interpret R², the slope, and the equation.
5. Check the model's assumptions using the residuals.

---

## 6. Results

### Regression statistics

| Statistic | Value | Meaning |
|---|---|---|
| Correlation (r) | −0.865 | Strong negative relationship |
| **R²** | **0.748** | Participation explains 74.8% of the variation in attrition |
| Adjusted R² | 0.741 | Fit after adjusting for the number of predictors |
| Standard error | 0.514 | Typical prediction error of about ±0.5 percentage points |
| F statistic | 101.11 | The model as a whole is significant |
| Observations | 36 | |

### Coefficients

| Term | Coefficient | Std. error | t | p-value | 95% CI |
|---|---|---|---|---|---|
| Intercept | 5.268 | 0.240 | 21.93 | 1.21 × 10⁻²¹ | 4.780 to 5.757 |
| **Participation rate** | **−0.0815** | 0.0081 | **−10.06** | **1.01 × 10⁻¹¹** | **−0.098 to −0.065** |

### Equation

> **Predicted attrition rate (%) = 5.268 − 0.0815 × participation rate (%)**

| Participation | Predicted monthly attrition |
|---|---|
| 10% | 4.45% |
| 25% | 3.23% |
| 44% (latest level) | 1.68% |

### Hypothesis test

The slope's p-value (1.01 × 10⁻¹¹) is far below α = 0.05, so we **reject H₀**. There is a statistically significant negative linear relationship between participation and attrition.

<img src="../Results/Program%20Participation%20Rate%20(%25)%20Line%20Fit%20Plot.png" width="650" alt="Scatter plot of participation rate vs. attrition rate with a downward fit line (y = −0.0815x + 5.2683, R² = 0.7484)">

<details>
<summary><b>Full Excel regression output</b></summary>

<br>

<img src="../Results/Linear%20Regression%20Summary%20Output.png" width="900" alt="Excel regression summary output, ANOVA table, coefficients, and residuals">

</details>

---

## 7. Model Diagnostics

| Check | Result | Assessment |
|---|---|---|
| **Linearity** | Points follow a straight downward line | ✅ Reasonable |
| **Independence of residuals** (Durbin-Watson) | 1.66 | ✅ Close to 2, so little month-to-month carryover in errors |
| **Normality of residuals** (Shapiro-Wilk) | p < 0.001 | ⚠️ Residuals aren't normal, mainly because of a few outlier months |
| **Outliers** | Month 14: 1.4% actual vs. 3.3% predicted · Month 12: 5.0% actual vs. 4.0% predicted | ⚠️ Worth investigating |

**Takeaway:** the outlier months make the exact p-value less precise, but the relationship is so strong (t = −10.06) that the conclusion holds.

---

## 8. Interpretation

- **Direction:** as participation goes up, attrition goes down.
- **Size:** each 1-percentage-point rise in participation is associated with about **0.08 points** lower monthly attrition. Moving from 15% to 40% participation lines up with attrition about **2 points lower** each month.
- **Strength:** with an R² of 0.748, participation accounts for most, but not all, of the change in attrition.
- **Practical meaning:** for a large nursing workforce, a 2-point monthly drop in attrition means many fewer departures, along with lower costs for recruiting, onboarding, and temporary staff.

---

## 9. Limitations

- **Correlation, not causation.** The analysis shows participation and attrition move together. It doesn't prove the program *caused* the drop.
- **Time is a hidden factor.** Participation rose almost steadily month after month, so it closely tracks the passage of time. Anything else that improved over the same period — pay, staffing levels, leadership, or the job market — could also explain lower attrition, and this model can't separate those effects.
- **About 25% of the variation is unexplained.** Factors such as workload, compensation, and job satisfaction aren't in the data.
- **Outlier months** affect the residuals (see Section 7).
- **One organization and program;** results may not generalize to other hospitals.

---

## 10. Recommendations

| # | Recommendation | Rationale |
|---|---|---|
| 1 | **Continue funding the program** | Participation is strongly linked to lower attrition |
| 2 | **Raise participation** with targeted promotion, fewer barriers (e.g., flexible scheduling), and incentives | Higher participation is associated with more retention |
| 3 | **Keep improving program content** using nurse feedback | Sustains engagement as the program grows |
| 4 | **Measure impact more rigorously:** compare participants with non-participants, and add data on workload, pay, and job satisfaction | Confirms whether the program itself drives the results, separate from other trends |
| 5 | **Investigate outlier months** (12 and 14) | May reveal events or practices that raise or lower attrition |
| 6 | **Use the equation for planning,** within the observed range (about 10%–44% participation) | Helps forecast staffing needs and set participation targets |

---

## 11. Conclusion

The data strongly supports a link between the Employee Well-being Program and nurse retention: as participation grew from about 15% to 40%, attrition fell by nearly half. The executive council has good reason to continue and expand the program, while adding better measurement to confirm how much of the improvement the program itself is responsible for.
