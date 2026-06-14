# Iris Flower Classification 🌸

This project classifies iris flowers into 3 species — **Setosa, Versicolor, and Virginica**  based on their petal and sepal measurements.

## What I did

1. **Loaded the data**  Used the built-in Iris dataset from scikit-learn.

2. **Explored the data**  Checked for nulls, duplicates, and basic stats. Found and removed 1 duplicate row.

3. **Visualized the data**  Made boxplots, histograms, and pie/count charts to understand the features and class distribution.

4. **Preprocessed**  Split the data into train/test sets (80/20, stratified) and scaled features using `StandardScaler`.

5. **Trained 4 models**  Logistic Regression, Random Forest, SVM, and XGBoost.

6. **Compared results**  Evaluated each model using accuracy, precision, recall, F1-score, and ROC-AUC.

7. **Picked the best model**  SVM gave the highest accuracy (96.7%), so I used it as my final model.

8. **Final evaluation**  Looked at the confusion matrix and ROC curves for the SVM model.

## Results

| Model | Accuracy |
|---|---|
| **SVM** | **96.7%** |
| Logistic Regression | 93.3% |
| XGBoost | 93.3% |
| Random Forest | 90.0% |

## Tools Used

- Python, Pandas, NumPy
- Scikit-learn, XGBoost
- Matplotlib, Seaborn

## How to Run

1. Install the requirements:
\`\`\`
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
\`\`\`

2. Open the notebook and run the cells in order.
