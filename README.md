# 🫁 Survey Lung Cancer Prediction using Random Forest Classifier

This project predicts the likelihood of lung cancer based on survey data using a **Random Forest Classifier**. The workflow includes preprocessing steps, outlier detection, label encoding, model training, and evaluation.

---

## 📁 Dataset

- **File Name:** `survey lung cancer.csv`
- **Target Variable:** `LUNG_CANCER`
- **Features Include:**
  - `GENDER`
  - `AGE`
  - Lifestyle & health-related survey responses (e.g., smoking, alcohol use, coughing, fatigue, etc.)

---

## 🔍 Project Workflow

### 1. 📥 Data Loading
- Data is read using `pandas`.
- Initial inspection with `.head()` and `.isnull().sum()`.

### 2. 🧼 Preprocessing
- Label Encoding is applied to:
  - `GENDER`
  - `LUNG_CANCER`
- Outliers in `AGE` are identified using Z-score method.
- Optional transformation for age (e.g., replacing values below 40) is commented out for flexibility.

### 3. 📊 Outlier Detection
- Visualized `AGE` distribution using a boxplot.
- Used `scipy.stats.zscore` to identify potential outliers in age.

### 4. 🧪 Train-Test Split
- Features and target variable are separated.
- Dataset is split into training and testing sets with `test_size=0.2`.

### 5. 🌳 Model Training
- A **Random Forest Classifier** is used:
  - `n_estimators=1000`
  - `max_depth=5`
  - `random_state=40`
  - `n_jobs=-1` for parallel processing

### 6. 📈 Model Evaluation
- Model performance is measured using **accuracy score**.

---

## 🛠️ Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `scipy`

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
