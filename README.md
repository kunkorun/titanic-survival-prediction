# Titanic Survival Prediction

In this project, I tackle the classic [Kaggle Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic) competition. The goal is to predict which passengers survived the disaster based on features like age, sex, ticket class, and family relationships.

While Titanic is often considered the "Hello World" of machine learning, my focus here was to build a rigorous, end-to-end supervised learning pipeline — from deep exploratory analysis and thoughtful feature engineering to robust cross-validation and final submission.

---

## Problem

This is a binary classification problem where the target variable is `Survived` (0 = No, 1 = Yes). The challenge lies in extracting meaningful signals from noisy, incomplete passenger data to accurately predict survival probabilities.

## Dataset

The project relies on the official Kaggle competition data:

- `train.csv` — training data containing passenger features and the target variable `Survived`
- `test.csv` — unlabeled test data used to generate the final Kaggle predictions

## Workflow

To ensure a structured and reproducible approach, I followed this complete machine learning pipeline:

1. Exploratory Data Analysis (EDA)
2. Data preprocessing and missing value imputation
3. Feature engineering
4. Model training and baseline comparison
5. Hyperparameter tuning
6. Cross-validation
7. Final model selection
8. Kaggle submission generation

## EDA

Before touching any models, I dug into the data to understand the underlying distributions and relationships. Using `matplotlib` and `seaborn`, I analyzed:

- the overall survival distribution
- the relationship between survival rates and key demographics like age, sex, and passenger class
- the impact of family size on survival chances
- feature correlations to identify potential multicollinearity

## Preprocessing and Feature Engineering

Raw data is rarely ready for modeling, so I spent a significant amount of time preparing the features. My main preprocessing steps included:

- handling missing values (using logical imputation strategies rather than just dropping rows)
- creating a `FamilySize` feature to capture the total number of relatives aboard
- creating an `IsAlone` binary flag to isolate solo travelers
- dropping unused or highly cardinal features that could cause overfitting
- one-hot encoding categorical variables
- applying feature scaling specifically for distance-based and linear models like Logistic Regression

## Models

I didn't want to just stick to one algorithm, so I trained and compared several classification models to see which one captured the data patterns best:

- Logistic Regression
- Decision Tree
- Gradient Boosting

To ensure my evaluation was robust and not dependent on a single train-test split, I evaluated model performance using **5-fold cross-validation**. Hyperparameter tuning was performed using both `GridSearchCV` and `RandomizedSearchCV` to find the optimal configurations for each algorithm.

## Evaluation

To get a comprehensive view of model performance, I tracked multiple metrics beyond just simple accuracy:

- Accuracy
- ROC-AUC
- Average Precision

All detailed experimental results, charts, and metric comparisons are documented inside the `titanic_final.ipynb` notebook.

## Final Model and Result

After extensive comparison and tuning, **Gradient Boosting** emerged as the strongest performer, striking the best balance between bias and variance.

| Metric | Result |
|---|---|
| Final Model | Gradient Boosting |
| Kaggle Public Score | 0.77990 |

Once the model was selected, I retrained it on the full training dataset and used it to generate the final `submission.csv` file for Kaggle.

## Repository Structure

```text
titanic-survival-prediction/
├── README.md
└── titanic_final.ipynb
```

## How to Run

### On Kaggle

1. Open the notebook in Kaggle
2. Add the Titanic competition dataset to the notebook environment
3. Open `titanic_final.ipynb`
4. Run all cells sequentially
5. The notebook will automatically generate and save `submission.csv`

### Locally

1. Install the required Python packages:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter
```

2. Launch Jupyter and open the notebook
3. Run the cells from top to bottom

## Possible Improvements

While the current pipeline is solid, there is always room to iterate. Possible directions for future experimentation include:

- implementing more advanced imputation techniques for missing values (like KNN or iterative imputation)
- extracting richer titles and statuses from the `Name` feature using regex
- testing advanced ensemble methods (like Stacking or Voting Classifiers)
- combining preprocessing and modeling into a single, leak-proof Scikit-Learn `Pipeline`
- exploring additional algorithms (like XGBoost or LightGBM) and more aggressive tuning strategies

## Tech Stack

- Python
- Jupyter Notebook
- pandas
- NumPy
- matplotlib
- seaborn
- scikit-learn
- SciPy

## Conclusion

For me, this project was an excellent exercise in solidifying a complete supervised learning workflow. It reinforced the importance of understanding the data deeply before modeling, preparing features thoughtfully, comparing models rigorously via cross-validation, and validating results before preparing a final submission.