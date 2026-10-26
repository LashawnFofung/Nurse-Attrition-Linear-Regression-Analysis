<div align="center">

# 🩺 Nurse Attrition Analysis
### Is a hospital's well-being program linked to lower nurse turnover?

**Linear Regression · Excel · Healthcare Analytics** · MBA, Data-Driven Decision Making

[![Presentation](https://img.shields.io/badge/Presentation-Watch-FF0000?style=flat&logo=youtube&logoColor=white)](https://youtu.be/mEK-_1xrKpA)
[![Report](https://img.shields.io/badge/Full_Report-Read-2EA44F?style=flat&logo=github&logoColor=white)](Report/Data%20Analysis%20Report.md)
[![Data Portfolio](https://img.shields.io/badge/Data_Portfolio-View-6E40C9?style=flat&logo=github&logoColor=white)](https://github.com/LashawnFofung/Data-Analysis-Portfolio)

</div>

---

## Contents
[TL;DR](#tldr) · [The Question](#the-question) · [Data](#data) · [Method](#method) · [Results](#results) · [What It Means](#what-it-means) · [Limitations](#limitations) · [Recommendations](#recommendations) · [Files](#files)

---

## TL;DR

| | |
|---|---|
| **Question** | Three years after launching an Employee Well-being Program, is higher participation associated with lower nurse attrition? |
| **Data** | 36 months of program participation rates and nurse attrition rates |
| **Method** | Simple linear regression in Excel |
| **Answer** | **Yes, strongly.** Participation explains **75%** of the month-to-month variation in attrition (p < 0.001). |
| **In practice** | Every **10-point** rise in participation is associated with about **0.8 points lower** monthly attrition |
| **Big picture** | Participation rose from **15% to 40%** (year 1 vs. year 3 averages) while attrition fell from **4.2% to 2.2%** |

---

## The Question

A healthcare system facing nurse shortages launched an **Employee Well-being Program** to reduce job stress and keep nurses from leaving. Three years later, the executive council needs to decide whether to keep funding it, and whether to expand it.

**Business question:** Is there a statistically significant relationship between how many nurses take part in the program and how many nurses leave?

---

## Data

36 monthly observations, provided by Western Governors University for the course (may be simulated).

| Variable | Role | Range |
|---|---|---|
| **Program participation rate (%)** | Independent (x) | 9.3% – 44.3% |
| **Nurse attrition rate (%)** | Dependent (y) | 1.4% – 5.0% |

| | Year 1 avg. | Year 2 avg. | Year 3 avg. |
|---|---|---|---|
| **Participation** | 15.4% | 27.8% | 39.9% |
| **Attrition** | 4.17% | 2.68% | 2.18% |

---

## Method

**Linear regression** fits a straight line through the data to measure how much attrition changes as participation changes, and whether that relationship is real or could be chance.

- **Null hypothesis (H₀):** there's no linear relationship between participation and attrition.
- **Significance level:** 0.05
- **Tool:** Excel Analysis ToolPak (Regression)

---

## Results

<img src="Results/Program%20Participation%20Rate%20(%25)%20Line%20Fit%20Plot.png" width="650" alt="Scatter plot of program participation rate vs. nurse attrition rate, with a downward-sloping fit line">

| Statistic | Value | Meaning |
|---|---|---|
| **R²** | **0.748** | Participation explains about 75% of the variation in attrition |
| **Slope** | **−0.0815** | Each 1-point rise in participation → about 0.08 points lower attrition |
| **95% confidence interval for slope** | −0.098 to −0.065 | The effect is clearly negative |
| **p-value** | **1.01 × 10⁻¹¹** | Far below 0.05 → reject H₀ |
| **Observations** | 36 months | |

**Equation:**
> Predicted attrition rate = 5.268 − 0.0815 × participation rate

| Participation | Predicted monthly attrition |
|---|---|
| 10% | 4.45% |
| 25% | 3.23% |
| 44% (latest level) | 1.68% |

<details>
<summary><b>Full regression output</b></summary>

<br>

<img src="Results/Linear%20Regression%20Summary%20Output.png" width="900" alt="Excel regression summary output">

</details>

---

## What It Means

- **The relationship is strong and real.** A p-value this small means the pattern is very unlikely to be chance.
- **It's meaningful in practice.** Going from 15% to 40% participation lines up with attrition dropping by about 2 points a month. For a large nursing staff, that's many nurses retained.
- **A few months stand out.** Month 14 had unusually low attrition (1.4% vs. 3.3% predicted), and month 12 unusually high (5.0%). These are worth investigating, since they may reflect events the model doesn't capture.

---

## Limitations

- **Correlation, not causation.** The data shows participation and attrition moving together, not that the program *caused* the drop.
- **Time is a hidden factor.** Participation rose almost steadily month after month, so it's nearly a stand-in for time. Anything else that improved over the same three years — pay, staffing, the job market — could also explain lower attrition. This model can't separate those effects.
- **25% is unexplained.** Other drivers, such as workload, compensation, and job satisfaction, aren't in the data.
- **One hospital system, one program.** Results may not apply elsewhere.

---

## Recommendations

| Recommendation | Why |
|---|---|
| **Continue funding the program** | Higher participation is strongly linked to lower attrition |
| **Grow participation** through promotion, fewer barriers (e.g., scheduling), and incentives | The relationship suggests more participation, more retention |
| **Keep improving program content** based on nurse feedback | Sustains engagement as participation grows |
| **Measure impact more rigorously** — compare participants with non-participants, and add workload, pay, and satisfaction data | Confirms whether the program itself is driving the results |

---

## Files

| File | What it is |
|---|---|
| [Excel workbook](Data/Nurse%20Attrition%20and%20Participation%20Program%20Data.xlsm) | Monthly data and regression output |
| [Data Analysis Report](Report/Data%20Analysis%20Report.md) | Objective, method, findings, and recommendations |
| [`Results/`](Results) | Regression output and line fit plot |
| 🎥 [Presentation](https://youtu.be/mEK-_1xrKpA) | Video walkthrough of the analysis |

<div align="center">

**Lashawn Fofung** · Technical Product Manager · [LinkedIn](https://www.linkedin.com/in/lashawnfofung/) · [Data Portfolio](https://github.com/LashawnFofung/Data-Analysis-Portfolio) · [All Projects](https://github.com/LashawnFofung/LashawnFofung-Portfolio)

</div>
