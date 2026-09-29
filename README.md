# 🚢 Titanic — Survival Prediction

This was my first end-to-end Machine Learning project on Kaggle.

The goal was to predict whether a passenger survived the Titanic disaster based on the available passenger information.

**Kaggle Score: 0.77990**

---

## 🎯 Goal

The main goal of this project was not only to get a good score, but to go through the full Machine Learning workflow:

* understand the dataset;
* perform EDA;
* handle missing values;
* create useful features;
* build a baseline;
* compare different models;
* validate the results;
* make a final Kaggle submission.

---

## 🔍 Exploratory Data Analysis

I started by looking at:

* missing values;
* distributions of the main features;
* relationships between features and the target;
* survival rates across different passenger groups.

One of the main things I noticed was that features such as **Sex, Pclass and Age** contain useful information about survival.

I used visualizations throughout the analysis to better understand the data and check whether my assumptions made sense.

---

## 🧹 Preprocessing & Feature Engineering

I experimented with:

* missing-value handling;
* categorical feature encoding;
* creating additional features;
* removing or transforming features where appropriate.

I tried to make preprocessing decisions based on what I found during EDA rather than applying the same transformations to every column automatically.

---

## 🤖 Models

I compared several Machine Learning approaches and used validation to compare their performance.

The main idea was to understand how the models behaved and whether a more complex model actually improved the result.

---

## 📊 Evaluation

The Kaggle competition uses **Accuracy** as the evaluation metric.

Final Kaggle score:

**0.77990**

The most important result for me was not the score itself, but learning how the different stages of the pipeline affected the final model.

---

## 🔎 What I Learned

This project gave me my first practical experience with the complete Data Science workflow.

The main things I learned were:

* how to approach an unfamiliar dataset;
* why EDA should influence modelling decisions;
* how missing values can affect a model;
* how to compare models using validation;
* why a working model is not necessarily a good model;
* how important it is to keep the whole workflow reproducible.

---

## 🚧 What I Would Improve

There are several things I would approach differently now.

After working on later projects, I would pay more attention to:

* making validation more robust;
* checking for possible leakage;
* documenting experiments more systematically;
* analysing model errors in more detail.

This project was my starting point, so one of the main goals was simply to learn the workflow and build a foundation for the next projects.

---

## ▶️ How to Run

Install the required dependencies:

```bash
pip install -r requirements.txt
```

Then open the notebook and run the project from the beginning.

---

## 🔗 Links

* **Kaggle:** [Titanic](https://www.kaggle.com/competitions/titanic)
* **My Kaggle Profile:** [kunkorun](https://www.kaggle.com/kunkorun)
