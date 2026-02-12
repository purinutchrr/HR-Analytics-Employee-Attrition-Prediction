# [cite_start] Google Advanced Data Analytics Capstone: Analyzing Employee Churn Risk [cite: 1]

[cite_start]**Author:** Purinut Chairungrueang [cite: 2]

## [cite_start] Project Overview [cite: 3]
[cite_start]This capstone project is part of the **Google Advanced Data Analytics Professional Certificate**[cite: 4]. [cite_start]The primary focus is to predict employee attrition by analyzing workplace factors and uncovering critical behavioral "red flags"[cite: 4, 5]. [cite_start]The goal is to move from reactive measures to data-driven retention strategies[cite: 6].



## [cite_start] Exploratory Data Analysis (EDA) & Key Insights [cite: 7, 8]
[cite_start]Before modeling, a thorough analysis was conducted on a refined dataset, including the removal of tenure outliers to focus on actionable trends[cite: 9, 10].

* [cite_start]**The Retention Danger Zone:** Employees are most likely to leave between their **3rd and 5th year**[cite: 23]. [cite_start]Resignations spike at year 3 and peak at year 5[cite: 24, 25].
* [cite_start]**U-Shaped Workload Risk:** Both under-worked (2 projects) and over-worked (6-7 projects) employees show high attrition[cite: 37, 38]. [cite_start]The "Sweet Spot" is **3-4 projects**[cite: 39].
* [cite_start]**Burnout of High Performers:** High performance does not guarantee retention[cite: 53]. [cite_start]A cluster of leavers consisted of high-performers (Evaluation > 0.8) working extreme monthly hours (>250)[cite: 54, 55, 56].



## [cite_start] Advanced Feature Engineering [cite: 272]
[cite_start]To create a more proactive HR tool, the model was refined to focus on **objective behavioral metrics** rather than subjective data[cite: 274].

* [cite_start]**Strategic Shift:** Dropped `satisfaction_level` to eliminate survey bias and lagging indicators[cite: 275, 277, 278].
* [cite_start]**The Burnout Index:** Developed a new feature ($Evaluation \times Monthly Hours$) to identify top talent at risk of exhaustion[cite: 281, 284, 285].
* [cite_start]**Hours Per Project:** Engineered to identify overwhelmed versus under-utilized employees[cite: 288, 290, 291].

## [cite_start] Model Evaluation [cite: 292]
[cite_start]The final **Random Forest** model was tuned using **4-fold cross-validation (CV=4)** to ensure stability and reliability[cite: 296, 297].

### [cite_start]Final Performance (Test Set - Random Forest 2) [cite: 298]
| Metric | Score | Interpretation |
| :--- | :--- | :--- |
| **Accuracy** | **97.26%** | [cite_start]High overall correctness in predicting employee status[cite: 299]. |
| **Precision** | **0.9407** | [cite_start]94% of predicted leavers actually leave (low false alarms)[cite: 299]. |
| **Recall** | **0.8916** | [cite_start]Successfully captures ~89% of actual attrition cases[cite: 299]. |
| **F1-Score** | **0.9155** | [cite_start]Excellent balance between Precision and Recall[cite: 299]. |
| **AUC-ROC** | **0.9402** | [cite_start]Strong ability to distinguish between "Stay" and "Left"[cite: 299]. |



## [cite_start] trategic Recommendations [cite: 300, 338]
* [cite_start]**Workload Rebalancing:** Use the **Burnout Index** to trigger capacity audits and redistribute tasks to ensure top talent is not over-leveraged[cite: 339].
* [cite_start]**Retention Focus (Year 3-5):** Conduct **"Stay Interviews"** at the 3-year mark to discuss career growth and re-engage talent before the critical 5-year exit window[cite: 340].
* [cite_start]**Optimal Project Load:** Maintain a "sweet spot" of **3-4 projects** per employee to balance engagement and prevent exhaustion[cite: 341].
