# HAnalytics: Predicting Employee Attrition (Salifort Motors) 📊

This project is the **Capstone Project** for the **Google Advanced Data Analytics Professional Certificate** on Coursera. It demonstrates an end-to-end data science workflow, from data cleaning and exploratory data analysis (EDA) to building and tuning predictive models.

## Project Objective
The goal of this project is to analyze a dataset from a fictional company, **Salifort Motors**, to identify the key factors driving employee turnover. By building a predictive model, aim to provide data-driven recommendations to help HR improve employee retention.

## 🛠️ Tech Stack & Tools
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn (Logistic Regression, Decision Tree, Random Forest)
- **Methodology:** Data Cleaning, EDA, Feature Engineering, Hyperparameter Tuning (GridSearchCV)

## Model Performance
After comparing multiple models, the **Random Forest Classifier** was identified as the best-performing model. It significantly outperformed Logistic Regression, especially in capturing employees who were likely to leave.

## Key Factors (Feature Importance)
1. **Satisfaction Level:** The strongest predictor. Low satisfaction is a major red flag for turnover.
2. **Workload (Overtime):** High average monthly hours and managing too many projects lead to burnout, increasing the likelihood of resignation.
3. **Tenure:** There is a critical point at 3–5 years where employees are most likely to leave.
4. **Last Evaluation:** The most recent performance score is a strong signal. Both very high and very low performers are at risk of leaving, suggesting that the company may be losing its top talent as well as those who may feel unsupported.

## Project Structure
- `HR_capstone.ipynb`: Full analysis, visualization, and modeling code.
- `HR_capstone_dataset.csv`: The synthetic dataset provided by Google.
- `README.md`: Project summary and insights.

**Author:** Purinut Chairungrueang
