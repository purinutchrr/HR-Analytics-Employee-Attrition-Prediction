# Google Advanced Data Analytics Capstone: Analyzing Employee Churn Risk

**Author:** Purinut Chairungrueang

## Project Overview
This project is part of the **Google Advanced Data Analytics Professional Certificate**. It focuses on predicting employee attrition using machine learning to identify red flags in behavior. By moving from reactive to proactive analysis, this model provides actionable insights for data-driven retention.

## Exploratory Data Analysis (EDA) & Key Insights
Based on the refined dataset (after removing tenure outliers), several critical patterns were identified:

* **The Retention Danger Zone:** Employees are most likely to leave between their **3rd to 5th year**. Resignations spike at year 3 and peak at year 5.
* **Workload U-Shape:** Attrition is highest for employees with either too few (2) or too many (6-7) projects. The Sweet Spot for stability is **3-4 projects**.
* **Burnout of High Performers:** High performance does not guarantee retention. A cluster of leavers consisted of high-performers (Evaluation > 0.8) working extreme monthly hours (>250 hours).
* **Satisfaction Threshold:** Employees with a satisfaction score below 0.4 are significantly more likely to leave, regardless of department or salary.

## Advanced Feature Engineering
To create a proactive monitoring tool, the model was refined to focus on **objective behavioral data** instead of subjective surveys.

* **Strategic Shift:** Dropped `satisfaction_level` to eliminate survey bias and lagging indicators.
* **The Burnout Index:** Engineered a new feature (`last_evaluation` * `average_monthly_hours`) to identify top talent at risk of exhaustion.
* **Workload Optimization:** Calculated `hours_per_project` to identify overwhelmed versus under-utilized employees.

## Model Performance
Three models were evaluated: Logistic Regression, Decision Tree, and Random Forest. The final **Random Forest** model, tuned with **4-fold cross-validation**, achieved high accuracy without relying on satisfaction scores.

### Final Results (Test Set)
| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Accuracy** | **97.26%** | High overall correctness in predicting status. |
| **Precision** | **0.9407** | 94% of predicted leavers actually leave. |
| **Recall** | **0.8916** | Captures ~89% of all actual attrition cases. |
| **F1-Score** | **0.9155** | Excellent balance between Precision and Recall. |
| **AUC-ROC** | **0.9402** | Strong ability to distinguish between "Stay" and "Left". |

## Strategic Recommendations
* **Workload Rebalancing:** Use the **Burnout Index** to trigger capacity audits and redistribute tasks, ensuring top talent is not over-leveraged.
* **Retention Focus (Year 3-5):** Conduct **Stay Interviews** at the 3-year mark to discuss career growth and re-engage talent before the 5-year exit window.
* **Optimal Project Load:** Maintain a sweet spot of **3-4 projects** per employee to balance engagement and prevent exhaustion.
