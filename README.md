\# Titanic Survival Prediction



A machine learning study project focused on predicting passenger survival on the Titanic.



The project includes a complete data workflow: exploratory data analysis (EDA), preprocessing, feature engineering, training and comparing machine learning models, and preparing the final submission for Kaggle.



\## Project Goals



\- Practice Exploratory Data Analysis (EDA) and data visualization skills

\- Implement Feature Engineering

\- Compare multiple machine learning algorithms

\- Master hyperparameter tuning using `GridSearchCV` and `RandomizedSearchCV`

\- Build a reproducible ML pipeline for preparing the final submission



\## Dataset



Dataset: \[Titanic - Machine Learning from Disaster](https://www.kaggle.com/c/titanic)



Files used:

\- `train.csv`

\- `test.csv`



\## Workflow



1\. Exploratory Data Analysis



Analyzed the distributions and relationships of features with the target variable `Survived`.



Key areas of analysis:

\- Distribution of survived and deceased passengers

\- Impact of age, sex, and ticket class on survival

\- Family size analysis

\- Investigation of correlations between features



`matplotlib` and `seaborn` were used for visualization.



2\. Data Preprocessing and Feature Engineering



The following steps were performed during data preparation:

\- Handling missing values

\- Creating `FamilySize` and `IsAlone` features

\- Dropping unused features

\- One-Hot Encoding of categorical variables

\- Feature scaling for Logistic Regression



3\. Modeling



The following algorithms were used for comparison:

\- Logistic Regression

\- Decision Tree

\- Gradient Boosting



Hyperparameter tuning was performed using `GridSearchCV` and `RandomizedSearchCV`.



5-fold cross-validation was applied for model evaluation.



4\. Model Evaluation



Models were compared on a hold-out test set.



The following metrics were used:

\- Accuracy

\- ROC-AUC

\- Average Precision



Experimental results are presented in the Jupyter Notebook.



5\. Final Model



After comparing the models, the best-performing model was trained on the full training dataset.



As a result, a `submission.csv` file was generated, ready for submission to Kaggle.



\## Results



\- Final Model: Gradient Boosting

\- Kaggle Score: 0.77990



\## How to Run the Project



\### Kaggle Notebook



1\. Open \[Kaggle Notebook](https://www.kaggle.com/code)

2\. Add the Titanic dataset

3\. Open the `titanic\_final.ipynb` file

4\. Run all cells (`Run All`)

5\. After execution, the `submission.csv` file will be created



\### Local Setup



Python and Jupyter Notebook are required to run the project locally.





```bash

pip install pandas numpy matplotlib seaborn scikit-learn scipy jupyter



```

After installing dependencies:



```bash

jupyter notebook

```



Open the `titanic\_final.ipynb` file and execute all cells.



\## Tech Stack



\- Python 3

\- Jupyter Notebook

\- pandas

\- NumPy

\- matplotlib

\- seaborn

\- scikit-learn

\- SciPy



\## Potential Improvements



\- More advanced handling of missing values

\- Extracting additional features from the `Name` column

\- Using ensemble methods

\- Combining preprocessing and modeling into a single Scikit-Learn Pipeline

\- Further model tuning and exploration of new algorithms



\---



P.S. This project is part of my machine learning journey and reflects my current stage of development in the field of Data Science.

