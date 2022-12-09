#  H&M Personalized Fashion Recommendations

# Titanic ML Challenge

Python notebooks containing two models proposed for the [H&M](https://www.kaggle.com/competitions/h-and-m-personalized-fashion-recommendations/) challenge hosted on Kaggle.

## Goal
  
The goal is to develop a recommender system that based on previous transactions and features from each customer it can predict which products he will buy next.

## The model

Two different model have been tried for the competition. The first is Alternating Least Squares, a type of matrix factorization algorithm, while for the second we did some feature engineering and we used LightGBM, a lite gradient boosting model.

## Candidate generation (only LGBM)

The candidates where generated by collecting the top12 items of the previous week and the last purchased basket (set of products) of the customer. To perform these operations **Pyspark** and its sql api were used.

## The performance

The performance was measured by Mean Average Precision. The ALS model reached around 0.007 MAP, while the LGBM model outperformed the previous one with a 0.012 MAP.
