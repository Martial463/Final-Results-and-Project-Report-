# Final-Results-and-Project-Report-
# Ontario School Board Graduation Analysis

This project examines whether selected secondary-school progress indicators can help identify Ontario school boards whose five-year graduation rates fall below the provincial benchmark of **89.5%**.

## Project Scope

The analysis uses three predictors:

- Grade 10 OSSLT achievement
- Grade 10 credit accumulation
- Grade 11 credit accumulation

The final modelling dataset contains **70 Ontario school boards**.

## Methods

The workflow includes:

- data validation and preprocessing
- descriptive statistics and visualizations
- Pearson correlation analysis
- binary classification using a majority baseline, logistic regression, and decision tree
- stratified 5-fold cross-validation
- repeated cross-validation for stability analysis
- confusion matrices and performance metrics
- training/testing time analysis
- logistic-regression coefficient analysis

## Key Results

Logistic regression was selected as the **champion model**.

| Model | Accuracy | Recall | F1 | Specificity |
|---|---:|---:|---:|---:|
| Majority Baseline | 0.571 | 1.000 | 0.727 | 0.000 |
| Logistic Regression | 0.800 | 0.850 | 0.829 | 0.733 |
| Decision Tree | 0.686 | 0.700 | 0.718 | 0.667 |

Logistic regression correctly classified **56 of 70 boards** and identified **34 of the 40 boards below benchmark**. Grade 11 credit accumulation was the strongest model contributor.

## Repository Structure

```text
data/
  raw/
  processed/

notebooks/
  01_data_preparation.ipynb
  02_exploratory_data_analysis.ipynb
  03_modelling_and_evaluation.ipynb
  04_stability_and_efficiency.ipynb

figures/
reports/

README.md
requirements.txt
```

## Reproducing the Analysis

Install the required packages:

```bash
pip install -r requirements.txt
```

Run the notebooks in numerical order from top to bottom.

The main environment uses:

```text
Python 3
pandas
numpy
matplotlib
scikit-learn
scipy
```

## Limitations

The analysis uses aggregated school-board data and only three predictors. Results should therefore be interpreted as **screening evidence rather than causal explanations**. The model is intended to support further investigation, not automatic decisions about board performance.

## GenAI Declaration

ChatGPT was used only to check the correctness and veracity of Python code. All code was executed and verified by me. Interpretation of results, methodological decisions, conclusions, and final comments were completed by me, and I take full responsibility for the submitted work.

## Author

**Martial Kaboré**  
Certificate in Big Data and Predictive Analytics  
Toronto Metropolitan University
