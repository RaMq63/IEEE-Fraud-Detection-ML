# IEEE-CIS Fraud Detection

## Project Overview

This project focuses on detecting fraudulent online financial transactions using the IEEE-CIS Fraud Detection dataset. Due to the highly imbalanced nature of the data, high dimensionality, and significant missing values, a robust machine learning pipeline was developed using tree-based supervised and unsupervised models.

The project applies extensive preprocessing, dimensionality reduction, and imbalance handling techniques, followed by multiple machine learning models to evaluate fraud detection performance from different perspectives.

---

## Dataset

The IEEE-CIS Fraud Detection dataset was obtained from Kaggle and consists of two main tables:

* **Transactions** dataset
* **Identity** dataset

Both datasets were merged using the `TransactionID` feature. After preprocessing, the final dataset contained over **590K records** and **434 features**.

📄 Detailed dataset description is available here:
➡️ [`docs/dataset_description.md`](docs/dataset_description.md)

---

## Theoretical Background

The project is formulated as a **binary classification problem**, where each transaction is classified as either fraudulent or non-fraudulent. Given the dataset characteristics, tree-based models and ensemble learning techniques were selected.

Theoretical explanations of all applied algorithms are documented, including:

* Random Forest
* XGBoost
* LightGBM
* Isolation Forest
* PCA
* SMOTE

📄 Full theoretical background:
➡️ [`docs/theoretical_background.md`](docs/theoretical_background.md)

---

## Methodology Overview

The complete machine learning pipeline includes:

* Data cleaning and merging
* Train–test splitting (80/20)
* Feature standardization
* Class imbalance handling using SMOTE
* Dimensionality reduction using PCA
* Training supervised and unsupervised models

📄 Full methodology details:
➡️ [`docs/methodology.md`](docs/methodology.md)

---

## Models Implemented

### Supervised Models

* Random Forest
* XGBoost (with SMOTE)
* XGBoost (using `scale_pos_weight`)
* LightGBM

### Unsupervised Model

* Isolation Forest

All supervised models were trained on PCA-transformed features.

---

## Results and Evaluation

Model performance was evaluated using:

* Accuracy
* Precision
* Recall
* F1-score
* ROC-AUC

XGBoost with `scale_pos_weight` achieved the best overall balance between precision and recall.

📄 Detailed results and evaluation:
➡️ [`docs/results_evaluation.md`](docs/results_evaluation.md)

---

## Discussion and Conclusion

The results demonstrate that **boosting-based models**, particularly XGBoost with proper imbalance handling, are highly effective for real-world fraud detection systems. The study also highlights the importance of evaluation metrics such as **F1-score** and **ROC-AUC** over accuracy in imbalanced classification problems.

📄 Full discussion and conclusion:
➡️ [`docs/discussion_conclusion.md`](docs/discussion_conclusion.md)

---

## Repository Structure

```text
IEEE-CIS-Fraud-Detection/
│
├── README.md
├── requirements.txt
├── .gitignore
│
├── notebooks/
│   ├── 01_data_loading.ipynb
│   ├── 02_eda.ipynb
│   ├── 03_preprocessing.ipynb
│   ├── 04_supervised_models.ipynb
│   ├── 05_unsupervised_models.ipynb
│   └── 06_evaluation.ipynb
│
├── docs/
│   ├── dataset_description.md
│   ├── theoretical_background.md
│   ├── pre_modeling.md
│   ├── methodology.md
│   ├── results_evaluation.md
│   └── discussion_conclusion.md
│
├── results/
│   ├── confusion_matrices.png
│   ├── roc_curves.png
│   └── metrics_table.csv
│
└── data/
    └── README.md
```

---

## How to Run the Project

1. Clone the repository

```bash
git clone https://github.com/your-username/IEEE-CIS-Fraud-Detection.git
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Run notebooks in order from the `notebooks/` directory

---

## Notes

* Raw dataset files are not included due to size and Kaggle licensing restrictions.
* Dataset can be downloaded directly from Kaggle: IEEE-CIS Fraud Detection.

---

## Author

This project was developed as an academic machine learning project focusing on fraud detection in large-scale financial datasets.

