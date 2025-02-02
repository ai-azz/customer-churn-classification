# Customer Churn Prediction (Supervised Learning)

## Project Description

This project aims to predict customer churn using machine learning techniques. Several supervised learning algorithms (K-Nearest Neighbors, Decision Tree, Random Forest, SVM, and Naive Bayes) are implemented and evaluated to identify customers at risk of leaving the service.

![Jupyter Notebook](https://img.shields.io/badge/Made%20with-Jupyter-orange?style=flat-square&logo=Jupyter)

## Dataset

**Source**: [Google Drive](https://drive.google.com/uc?id=19IfOP0QmCHccMu8A6B2fCUpFqZwCxuzO)

**Size**: 10,000 records

**Features**:

| Feature | Description |
| --- | --- |
| CreditScore | Customer's credit score |
| Geography | Customer's location (France/Spain/Germany) |
| Gender | Male/Female |
| Age | Customer's age |
| Tenure | Years as bank customer |
| Balance | Account balance |
| NumOfProducts | Number of bank products used |
| HasCrCard | Credit card ownership (1/0) |
| IsActiveMember | Active membership status (1/0) |
| EstimatedSalary | Estimated salary |
| **Exited** (Target) | Churn status (1=Churned, 0=Retained) |

## Installation

```bash
pip install pandas numpy scikit-learn matplotlib seaborn
```

## Usage

### 1. Data Preprocessing

- **Handling Categorical Data**: `LabelEncoder` for Geography/Gender
- **Feature Scaling**: `StandardScaler`/`MinMaxScaler`
- **Train-Test Split**: 80-20 ratio

### 2. Models Implemented

```python
models = {
    "KNN": KNeighborsClassifier(),
    "Decision Tree": DecisionTreeClassifier(),
    "Random Forest": RandomForestClassifier(),
    "SVM": SVC(),
    "Naive Bayes": GaussianNB()
}
```

### 3. Evaluation Metrics

- Confusion Matrix
- Accuracy
- Precision
- Recall
- F1-Score

## Results

| **Model** | **Accuracy** | **Precision** | **Recall** | **F1-Score** |
| --- | --- | --- | --- | --- |
| Random Forest | 0.86 | 0.59 | 0.32 | 0.41 |
| SVM | 0.85 | 0.82 | 0.31 | 0.45 |
| KNN | 0.82 | 0.59 | 0.32 | 0.42 |
| Naive Bayes | 0.82 | 0.68 | 0.23 | 0.35 |
| Decision Tree | 0.78 | 0.45 | 0.51 | 0.48 |

**Best Performing Model**: Random Forest

## Key Findings from EDA

- Churn rate: ~20%
- Strong correlation between Age/Balance and churn
- Active members show lower churn probability

## How to Run

1. Download dataset from [Google Drive](https://drive.google.com/uc?id=19IfOP0QmCHccMu8A6B2fCUpFqZwCxuzO)
2. Upload to Google Colab or local Jupyter environment
3. Execute cells sequentially