# osu_hackai
# House Price Prediction Analysis Overview

## Team Name: Triple C
## Team Member: Hao-Chun Chou, Lillian Chen, Larry Chen
## Challenge: AI Club Track (House Price Prediction)

## Project Summary
This project aimed to predict house prices by analyzing a dataset with various attributes such as area, number of bedrooms, bathrooms, and more. We conducted our analyses using two primary tools: PySpark and Scikit-learn, to compare different models and identify the most effective approach for predicting house prices.

## Data Preparation
Our dataset comprised 327 records with no missing values, duplicates, or inconsistencies. Although we considered removing outliers, we ultimately retained the full dataset to avoid losing valuable information, given its limited size.

## Feature Engineering
In both PySpark and Scikit-learn, we transformed categorical variables into numeric formats. This involved using StringIndexer in PySpark and manual encoding methods in Scikit-learn. Features underwent binary and ordinal encoding where applicable, and we applied log transformations to 'price' and 'area' to normalize their distributions. A feature, "price per sqft," was initially considered but excluded due to its potential to mislead the model, as it implicitly contains the target variable.

## Model Selection and Performance
The Gradient Boosting (GB) model implemented in Scikit-learn was the standout, achieving an R^2 of 0.687. Although we experimented with neural networks, their performance was significantly poorer, likely due to the dataset's small size, illustrating the challenges of using deep learning in this context.

## Conclusions
 - The GB model in Scikit-learn provided the highest accuracy in our experiments.
 - The project highlighted the importance of judicious feature selection, particularly in avoiding features that could lead to overfitting.
 - The limited dataset size was a key challenge, especially for more complex models like neural networks, indicating the need for larger datasets for these approaches.

## Future Directions
Further research could involve acquiring more data to enhance the dataset and potentially improve model performance. Additionally, exploring alternative feature engineering techniques and model parameters may offer insights into achieving better results.

