# Lead Conversion Scoring — Logistic Regression
## Project explanation and interview preparation

### Project summary

This project builds a binary classification model for X Education to identify leads that are more likely to convert into customers. The work includes data cleaning, exploratory analysis, categorical encoding, feature selection and logistic regression. A lead score can help sales teams prioritise follow-up, provided the probability threshold reflects business costs.

**60-second interview pitch**

“I worked on a lead-scoring case study for X Education. The sales team wanted a better way to prioritise leads, so I prepared the data, handled missing and low-information fields, encoded categorical variables and built a logistic regression classifier. I used feature selection and multicollinearity checks to create an interpretable model, then evaluated it on a held-out test set using accuracy, sensitivity, specificity, precision, recall and ROC-AUC. The business step is choosing a threshold based on the cost of missing a likely customer versus spending time on a low-probability lead.”

### Business problem

Sales teams have limited follow-up capacity. The objective is to rank leads by conversion likelihood so that high-potential prospects receive timely attention. The assignment's approximate 80% conversion target is a business aspiration; it is not the same as model accuracy or the percentage of leads predicted to convert.

### Data preparation and modelling

The project records the following steps:

- Checked duplicate records and excluded identifiers such as Prospect ID and Lead Number from the predictors.
- Replaced placeholder values such as “Select” with missing values.
- Considered removing columns with more than 40% missing values.
- Reviewed categorical and numerical variables, distributions and correlations.
- Grouped similar categories and created indicators such as “Not Tagged” where missingness carried information.
- Encoded binary and categorical variables and standardised numeric features.
- Used a train/test split, logistic regression, recursive feature elimination, p-value review and VIF diagnostics.
- Generated probabilities and lead scores, then evaluated classification performance.

Missing-value handling should be field-specific. Missingness can itself be informative in some business fields, but that should be tested rather than assumed.

### Results recorded

The existing project summary reports test accuracy of 92.51%, sensitivity of 91.39%, specificity of 93.2% and ROC-AUC of 0.97. It also records a 0.30 probability threshold. Verify all figures and the final threshold against the notebook before quoting them in interviews.

### Interview questions and suggested answers

**1. Why logistic regression for lead scoring?**  
It is a classification method that estimates the probability of a binary outcome. It is relatively interpretable and provides a probability score that can be used to rank leads.

**2. What does the logistic function do?**  
It maps a linear combination of predictors to a value between 0 and 1, which can be interpreted as a predicted probability under the model.

**3. What is the difference between a probability and a classification?**  
A probability is the model's estimated likelihood. A classification is produced after applying a threshold to that probability. Changing the threshold changes the balance between false positives and false negatives.

**4. What is sensitivity?**  
Sensitivity, or recall for the positive class, is the proportion of actual converters correctly identified by the model.

**5. What is specificity?**  
Specificity is the proportion of actual non-converters correctly identified.

**6. What is precision?**  
Precision is the proportion of leads predicted as converters that actually convert. It matters when sales capacity is limited and false-positive follow-ups are costly.

**7. Why is accuracy not enough?**  
Accuracy can be misleading when classes are imbalanced or when the costs of false positives and false negatives differ. Precision, recall, specificity, F1 and ROC-AUC give a fuller picture.

**8. What does ROC-AUC measure?**  
It summarises how well the model ranks positive cases above negative cases across thresholds. It does not identify the best operational threshold by itself.

**9. What is RFE?**  
Recursive Feature Elimination repeatedly fits a model, ranks features and removes the least useful features until a chosen feature set remains.

**10. What is VIF?**  
VIF quantifies how much the variance of a coefficient is inflated by linear relationships among predictors. High values suggest multicollinearity that may make coefficients unstable.

**11. How should the classification threshold be chosen?**  
Choose it according to business costs and operational capacity. For lead scoring, the cost of missing a likely customer should be balanced against the cost of following up with a lead that does not convert.

**12. How would you validate the model further?**  
Check class balance, compare with a baseline, inspect calibration and the confusion matrix, use cross-validation where appropriate and confirm that the test set was not used to select features or tune the threshold.

### Business recommendations recorded in the project

The original analysis highlights references and the Welingak website, Google/direct traffic, SMS engagement and email opens as areas to investigate. Treat these as patterns in the assignment data, not causal claims that a channel will necessarily improve conversion.

### Limitations to be ready to discuss

- Verify reported performance values against the final notebook and split.
- Confirm that feature selection and threshold tuning did not use the held-out test data.
- Assess class balance and probability calibration.
- Threshold choice should reflect actual sales capacity and the cost of errors.
- Association between a lead attribute and conversion does not prove causation.

### Resume bullet

Built a logistic regression lead-scoring model for an education case study, using data cleaning, feature selection, multicollinearity diagnostics and classification metrics to support sales lead prioritisation.

### Files

- [Modelling notebook](../Lead%20Scoring%20CS%20EDM.ipynb)
- [Summary report](../Lead%20Scoring%20Case%20Study%20Summary%20Report.pdf)
- [Presentation](../Lead%20Score%20Case%20Studyppt.pdf_compressed.pdf)
- [Assignment questions](../Assignment%20Subjective%20Questions%20EDM.pdf)
