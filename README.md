# AI-Development-Workflow
# AI Development Workflow – Hospital Readmission Prediction

This repository showcases a comprehensive approach to building an AI system for predicting patient readmission within 30 days of discharge. The project is structured to reflect an end-to-end development pipeline guided by critical thinking, ethical awareness, and technical rigor.


##  Assignment Structure Overview

This repository fulfills the requirements of the **AI Development Workflow Assignment**. The task is divided into four main parts:

1. **Short Answer Questions** (30 points)
2. **Case Study Application** (40 points)
3. **Critical Thinking** (20 points)
4. **Reflection & Workflow Diagram** (10 points)


## Part 1: Short Answer Questions

### 1. Problem Definition (6 points)

- **Hypothetical AI Problem**: Predicting crop diseases before their onset.


### 2. Data Collection & Preprocessing (8 points)


### 3.  Model Development (8 points)

- **Chosen Model**: A Convolutional Neural Network (CNN) for image classifications due to its ability to automatically detect features such as shapes and textures.


- **Data Splitting**:
  - 70% Training
  - 15% Validation
  - 15% Test 

- **Hyperparameters to Tune**:
  1. Number of trees
  2. Maximum depth — balances accuracy and computational load



### 4.  Evaluation & Deployment (8 points)

- **Evaluation Metrics**:
  1. Accuracy – Overall performance.
  2. F1 Score – Useful for imbalanced dropout classes.



##  Part 2: Case Study – Hospital Readmission Prediction (40 points)

###  Problem Scope (5 points)
- **Definition**: Predicting patient readmission risk within 30 days of discharge.
- **Objectives**:
  1. Identify high-risk patients.
  2. Enable preventive care planning.
  3. Reduce hospital costs and improve care.
- **Stakeholders**:
  - Hospital Administrators
  - Care Managers and Physicians


### Data Strategy (10 points)

- **Data Sources**:
  - EHRs (diagnosis, labs, medications)
  - Demographics (age, location, insurance type)

- **Ethical Concerns**:
  1. Patient privacy (HIPAA)
  2. Bias toward underserved groups

- **Preprocessing Pipeline**:
  - Impute missing values
  - Normalize continuous features
  - Engineer features: prior admissions, discharge diagnosis flags

---

###  Model Development (10 points)

- **Model**: Random Forest — good for explainability and performance on structured clinical data

- **Confusion Matrix (Hypothetical)**:

|                | Predicted: No | Predicted: Yes |
|----------------|---------------|----------------|
| Actual: No     | 80            | 20             |
| Actual: Yes    | 10            | 90             |

- **Precision**: 81.8%  
- **Recall**: 90.0%


###  Deployment (10 points)

- **Integration Steps**:
  1. Package model via API
  2. Link to hospital EHR systems
  3. Create dashboard for clinicians

- **Compliance Measures**:
  - Encrypt PHI data
  - Apply access control
  - Maintain audit logs and privacy documentation



###  Optimization (5 points)

- **Method**: L2 regularization to reduce overfitting by penalizing large weight values in model training.



##  Part 3: Critical Thinking (20 points)

### Ethics & Bias (10 points)

- **Risk**: If training data is skewed toward certain demographics, predictions may reinforce disparities.

- **Mitigation Strategy**: Fairness audits + rebalancing via SMOTE or sample weighting.



###  Trade-offs (10 points)

- **Interpretability vs Accuracy**:
  - Logistic Regression: easy to explain
  - Deep Learning: better accuracy but low transparency

- **Impact of Limited Resources**:
  - Prefer lightweight models or cloud deployment
  - Avoid GPU-heavy frameworks unless infrastructure supports it



##  Part 4: Reflection & Diagram (10 points)

### Reflection (5 points)

- **Challenge**: Data preprocessing — structuring messy EHRs with missing fields and inconsistent formats.

- **Improvement**: Use automated pipelines and domain expertise to refine feature engineering and audit fairness.



###  AI Development Workflow Diagram (5 points)

```text
[ Problem Definition ]
       ↓
[ Data Collection & Preprocessing ]
       ↓
[ Model Selection & Training ]
       ↓
[ Model Evaluation ]
       ↓
[ Deployment ]
       ↓
[ Optimization ]
       ↓
[ Ethics & Bias Mitigation ]
       ↓
[ Final Reflection ]
