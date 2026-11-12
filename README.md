# Lead Conversion Scoring — Logistic Regression

A classification case study for X Education, focused on identifying leads with a higher likelihood of converting so that sales teams can prioritise follow-up.

**Tools:** Python · Pandas · NumPy · scikit-learn · statsmodels · Seaborn

## Business question

How can a sales team use lead attributes and engagement signals to prioritise follow-up when its time and outreach capacity are limited?

## Approach

1. **Data preparation** — reviewed duplicates, identifiers, placeholder values and missingness.
2. **Exploratory analysis** — examined categorical and numerical variables, distributions, correlations and outliers.
3. **Feature preparation** — binary mapping, dummy encoding and standardisation of numeric variables.
4. **Model building** — logistic regression, recursive feature elimination (RFE), p-value review and VIF diagnostics.
5. **Evaluation** — assessed accuracy, sensitivity, specificity, precision, recall and ROC-AUC; selected a probability threshold for lead prioritisation.

## Results recorded in the project

The existing project summary reports a test accuracy of **92.51%**, sensitivity of **91.39%**, specificity of **93.2%**, and ROC-AUC of **0.97**. It also records a 0.30 probability threshold in the training analysis.

These figures should be checked against the final notebook and evaluation split before being used externally. Accuracy alone is not enough to judge a lead-scoring model.

## Business interpretation

A lead score can help rank prospects for follow-up. The operating threshold should reflect the cost of missing a likely customer versus the time spent contacting a low-probability lead. Conversion rate, model accuracy and the business target mentioned in the case study are different measures and should not be confused.

## Repository contents

- `Lead Scoring CS EDM.ipynb` — modelling notebook.
- `Lead Scoring Case Study Summary Report.pdf` — summary report.
- `Lead Score Case Studyppt.pdf_compressed.pdf` — project presentation.
- `Assignment Subjective Questions EDM.pdf` — assignment questions.
- `docs/PROJECT_GUIDE_AND_INTERVIEW_QUESTIONS.md` — explanation and interview preparation.

## Interview preparation

See [Project explanation and interview questions](docs/PROJECT_GUIDE_AND_INTERVIEW_QUESTIONS.md).

## Author

**Eshwar Ramesh** · [GitHub](https://github.com/EshwarRamesh7) · [Portfolio](https://eshwarrameshportfolio.netlify.app) · [LinkedIn](https://www.linkedin.com/in/eshwar-ramesh-9a4652251)
