# Bank Marketing Classification

This project evaluates different classification models on a dataset related to marketing bank products via telephone. The goal is to compare the performance of various classifiers and optimize them using hyperparameter tuning.

## Dataset
The dataset contains customer information and details about the last contact during a marketing campaign. Features include:
- **Numerical:** `age`, `duration`
- **Categorical:** `job`, `marital`, `education`, `default`, `housing`, `loan`, `contact`, `month`, `day_of_week`
- **Target:** `y` (whether the customer subscribed to a term deposit)

## Models Used
1. **Logistic Regression**
2. **K-Nearest Neighbors (KNN)**
3. **Decision Tree**
4. **Support Vector Machine (SVM)**

## Performance Metrics
Models are evaluated using:
- **Precision**
- **Recall**
- **Train & Test Accuracy**
- **Training Time**

### Best Hyperparameters:
- **KNN:** `n_neighbors = 9`
- **Decision Tree:** `max_depth = 3`

### Results:
| Model                 | Train Time | Train Accuracy | Test Accuracy | Precision | Recall  |
|----------------------|------------|---------------|--------------|----------|---------|
| Logistic Regression | 0.1197 sec  | 59.13%        | 58.47%       | 15.84%   | 62.28%  |
| KNN                 | 0.0040 sec  | 88.95%        | 88.55%       | 42.72%   | 4.74%   |
| Decision Tree       | 0.0141 sec  | 88.79%        | 88.73%       | 50.00%   | 2.58%   |
| SVM                 | 26.58 sec   | 62.65%        | 60.84%       | 16.50%   | 60.99%  |

### Findings:
If we care about detecting positives (high recall): Choose Logistic Regression or SVM. Logistic has much shorter training time.
If we care about overall accuracy and precision: Choose Decision Tree. 
If we care about speed and simplicity: KNN is extremely fast with ok accuracy.