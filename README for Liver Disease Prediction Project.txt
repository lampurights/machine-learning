## Project Overview
This project involves predicting liver disease based on patient data from the `indian_liver_patient.csv` dataset. The objective is to classify patients into two categories:
- **1**: Patients with liver disease.
- **2**: Patients without liver disease.

The dataset includes features such as age, gender, and various biochemical test results.

---

## Requirements
### Libraries Used
1. `numpy`
2. `pandas`
3. `matplotlib`
4. `seaborn`
5. `sklearn`
6. `%matplotlib inline`

Install the necessary libraries using pip:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## Steps Followed

### 1. **Data Loading and Preprocessing**
- Loaded the dataset from `indian_liver_patient.csv`.
- Column names were converted to lowercase for consistency.
- Handled missing values by filling them with the mean value for `albumin_and_globulin_ratio`.
- Encoded the `gender` column using `LabelEncoder`.
- Scaled numerical features using `RobustScaler` for better handling of skewness.
- Log-transformed skewed features (`albumin_and_globulin_ratio`, `total_bilirubin`, `alkaline_phosphotase`, `alamine_aminotransferase`).

### 2. **Balancing the Dataset**
- The dataset was imbalanced with:
  - 416 entries for class `1`.
  - 167 entries for class `2`.
- Applied upsampling to balance the minority class (class `2`).

### 3. **Model Training and Evaluation**
#### Models Used:
1. **Logistic Regression**
   - Achieved ~64% accuracy on the test set.
   - ROC-AUC score: ~0.64.
2. **Support Vector Classifier (SVC)**
   - Achieved ~68% accuracy on the test set.
   - ROC-AUC score: ~0.68.
3. **Decision Tree Classifier**
   - Achieved ~84% accuracy on the test set.
   - ROC-AUC score: ~0.83.
   - High train accuracy suggests potential overfitting.

#### Evaluation Metrics:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-Score**
- **ROC-AUC Score**
- **Confusion Matrix**

### 4. **Results**
- Decision Tree Classifier provided the best test accuracy and ROC-AUC score but displayed signs of overfitting.
- Logistic Regression and SVC performed reasonably well but were less prone to overfitting.

---

## How to Run the Code
1. Clone this repository or download the script.
2. Ensure the dataset `indian_liver_patient.csv` is in the same directory as the script.
3. Run the Python script:
   ```bash
   python liver_prediction.py
   ```

---

## Future Improvements
1. **Feature Engineering**:
   - Derive new features from existing ones to improve model performance.
2. **Advanced Models**:
   - Explore ensemble methods like Random Forests or Gradient Boosting.
3. **Hyperparameter Tuning**:
   - Fine-tune hyperparameters for better performance.
4. **Cross-Validation**:
   - Implement k-fold cross-validation to assess model robustness.

---

## References
- Dataset source: [Indian Liver Patient Dataset on UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/ILPD+%28Indian+Liver+Patient+Dataset%29)
- Documentation for Python libraries:
  - [Scikit-Learn](https://scikit-learn.org/)
  - [Pandas](https://pandas.pydata.org/)
  - [Seaborn](https://seaborn.pydata.org/)
  - [Matplotlib](https://matplotlib.org/)


