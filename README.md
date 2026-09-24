# KNN and Naive Bayes Model Comparison

This project comes from a university group machine learning project that compared different learning algorithms using two datasets: Online Retail and Credit Card Fraud Detection.

My main contribution was the **K-Nearest Neighbours (KNN)** and **Naive Bayes** experiments. I worked on both datasets, including model training, hyperparameter checking, evaluation and comparison of the results.

## My Work

I focused on:

- implementing KNN for Online Retail and Credit Card Fraud Detection
- implementing Naive Bayes for both datasets
- checking KNN hyperparameters and model behaviour
- comparing model performance across the two datasets
- evaluating accuracy, precision, recall, F1-score and ROC-AUC
- analysing confusion matrices and ROC curves
- comparing the strengths and limitations of KNN and Naive Bayes

## Datasets

The datasets used for the experiments are included in the `dataset/` folder.

### Online Retail

`dataset/online_retail_II.xlsx`

The Online Retail dataset contains transaction data and was used to classify lower-value and higher-value purchasing behaviour using prepared transaction features.

### Credit Card Fraud Detection

`dataset/creditcard.csv`

The Credit Card dataset contains anonymised transaction features and a binary fraud label. Since fraudulent transactions are heavily outnumbered by normal transactions, I evaluated the models using precision, recall, F1-score and ROC-AUC alongside accuracy.

## My Model Results

| Model | Dataset | Accuracy | Precision | Recall | F1-score | ROC-AUC |
|---|---|---:|---:|---:|---:|---:|
| KNN | Online Retail | 0.8263 | 0.7065 | 0.5221 | 0.6005 | 0.7749 |
| KNN | Credit Card | 0.9993 | 0.8590 | 0.7052 | 0.7746 | 0.8734 |
| Naive Bayes | Online Retail | 0.3283 | 0.2646 | 0.9478 | 0.4137 | 0.7791 |
| Naive Bayes | Credit Card | 0.9927 | 0.1377 | 0.6421 | 0.2267 | 0.9562 |

KNN gave a much stronger balance between precision and recall for the credit card fraud task. Naive Bayes achieved useful recall and a high ROC-AUC on the fraud dataset, but its lower precision meant that it produced more false positives.

## Overall Group Project

The full group project compared eleven machine learning and data mining approaches:

- Decision Tree
- Support Vector Machine
- Naive Bayes
- K-Means
- K-Nearest Neighbours
- Perceptron
- Decision Stump
- Multi-Layer Perceptron
- Evolutionary LCS
- Q-Learning
- ILP-style learning

In the final group comparison, **Decision Tree was selected as the strongest model based on F1-score for both datasets**. KNN was also one of the stronger models, particularly for credit card fraud detection, where it provided a good balance between precision and recall.

The overall results also showed why a model should not be judged using accuracy alone, especially for highly imbalanced fraud data.

## Technologies Used

- Python
- Jupyter Notebook
- pandas
- NumPy
- scikit-learn
- Matplotlib
- Seaborn
- K-Nearest Neighbours
- Naive Bayes
- Hyperparameter tuning
- Confusion matrices
- ROC-AUC

## Project Structure

```text
knn-naive-bayes-comparison/
├── dataset/
│   ├── creditcard.csv
│   └── online_retail_II.xlsx
├── notebooks/
│   ├── Knn_credit.ipynb
│   ├── Knn_retail.ipynb
│   ├── Knn_retail_credit_comparison.ipynb
│   ├── Knn_analysis_summary.ipynb
│   ├── Naive_Bayes_credit.ipynb
│   ├── Naive_Bayes_retail.ipynb
│   ├── Naive_Bayes_retail_credit_comparison.ipynb
│   └── Naive_Bayes_analysis_summary.ipynb
├── results/
│   ├── Knn_credit_results.csv
│   ├── Knn_retail_results.csv
│   ├── Knn_retail_credit_comparison.csv
│   ├── Naive_Bayes_credit_results.csv
│   ├── Naive_Bayes_retail_results.csv
│   └── Naive_Bayes_retail_credit_comparison.csv
├── .gitignore
├── LICENSE
└── README.md
```

## What I Learned

This project helped me understand how the same machine learning algorithm can behave very differently depending on the dataset and class distribution.

The fraud detection task was especially useful because very high accuracy did not necessarily mean that a model was good at detecting fraud. Comparing precision, recall, F1-score, ROC-AUC and confusion matrices gave me a much better understanding of model evaluation for imbalanced datasets.

Working with KNN also helped me understand the effect of neighbour selection, distance measures and feature scaling, while Naive Bayes gave me a useful comparison with a simpler probabilistic approach.

## License

This project is licensed under the MIT License.
