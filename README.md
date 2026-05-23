# 📉 Customer Churn Prediction — Telco Dataset

> A machine learning project that predicts customer churn for a telecom company using classical ML models and a custom PyTorch Neural Network.

---

## 📌 About

Customer churn is one of the most costly problems in the telecom industry. This project builds and compares multiple predictive models on the **Telco Customer Churn** dataset to identify customers who are likely to leave — enabling proactive retention strategies.

---

## 📓 Notebook Structure

| Section | Description |
|---|---|
| **1. Data Loading & Preprocessing** | Load CSV, drop irrelevant columns, encode categoricals, scale features, train-test split |
| **2. Exploratory Data Analysis** | Churn distribution, tenure, monthly & total charges, correlation heatmap |
| **3. Machine Learning Models** | Logistic Regression, Decision Tree, Random Forest — with classification report & ROC-AUC |
| **4. Neural Network** | Custom PyTorch feedforward network (ChurnNN) trained with BCE loss & Adam optimiser |

---

## 🧠 Models Used

| Model | Library |
|---|---|
| Logistic Regression | scikit-learn |
| Decision Tree Classifier | scikit-learn |
| Random Forest Classifier | scikit-learn |
| Neural Network (ChurnNN) | PyTorch |

### ChurnNN Architecture
```
Input → Linear(32) → ReLU → Linear(16) → ReLU → Linear(1) → Sigmoid
```
- Loss: Binary Cross Entropy (`BCELoss`)
- Optimiser: Adam (lr = 0.001)
- Epochs: 50, Batch size: 64

---

## 📊 Evaluation Metrics

All models are evaluated using:
- Confusion Matrix
- Classification Report (Precision, Recall, F1-score)
- ROC-AUC Score

---

## 📁 Dataset — `Telco_Churn.csv`

**Target variable:** `Churn Value` (0 = No Churn, 1 = Churned)

**Dropped columns:** `Churn Reason`, `CustomerID`, `Country`, `State`, `City`, `Zip Code`, `Lat Long`

**Preprocessing steps:**
- Label encoding for all categorical columns
- Standard scaling (`StandardScaler`) on all features
- 80/20 train-test split (`random_state=42`)

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Language | Python 3 |
| Data | Pandas, NumPy |
| Visualisation | Matplotlib, Seaborn |
| ML Models | scikit-learn |
| Deep Learning | PyTorch |
| Environment | Google Colab / Jupyter Notebook |

---

## 🚀 Getting Started

### 1. Clone the repo

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn torch
```

### 3. Add the dataset

Place `Telco_Churn.csv` in `/content/` (Colab) or update the path in the notebook:

```python
df = pd.read_csv("Telco_Churn.csv")
```

### 4. Run the notebook

Open the `.ipynb` file in **Google Colab** or **Jupyter Notebook** and run all cells.

---

## 👩‍💻 Author

**Ayeshi Jayarathna**
