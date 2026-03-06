# Customer Churn Prediction using Big Data Analytics

## Project Overview
Customer retention is a major challenge for subscription-based services. Acquiring a new customer is significantly more expensive than retaining an existing one. This project focuses on predicting customers who are likely to cancel their subscription.

The project analyzes large-scale user interaction data from **Sparkify**, an imaginary digital music streaming service similar to Spotify. The dataset contains **12GB of user activity logs** and is used to build machine learning models that can identify users likely to churn.

---

## Problem Statement
Acquiring new customers is more costly than retaining existing ones. The goal of this project is to identify users who are likely to churn so that businesses can take preventive actions and improve customer retention.

---

## Dataset
The dataset consists of **12GB of user interaction logs** from Sparkify.

You can download it from here:
[https://drive.google.com/file/d/1eVXe5774gjmb-SeZRC9Q_p2J_zwlVk0p/view?usp=sharing]
It contains information such as:
- User activity logs
- Songs played
- Likes and dislikes
- User sessions
- Playlist activity
- Page interactions

Churned users were identified based on user behavior, particularly when a user visited the **Cancellation Confirmation** page.

---

## Data Preprocessing

The following preprocessing steps were performed:

- Removal of unnecessary columns  
  - Firstname  
  - Lastname  
  - Id_copy  

- Unit conversion  
  - Registration and timestamp values were converted from **milliseconds to seconds**

- Churn label creation  
  - A new column **label** was created  
  - `1` indicates churned user  
  - `0` indicates active user

- Dataset filtering and cleaning

---

## Feature Engineering

Meaningful features were extracted from user activity logs to improve model performance.

Features used in the model include:

- Time since registration
- Number of friends referred
- Total songs listened to
- Total songs liked
- Total songs disliked
- Number of songs in user playlist
- Average songs played
- Number of artists listened to
- Number of user sessions logged

Some features were removed after observing **less than 1% importance during model training**.

---

## Modeling Approach

The dataset was split into **80% training and 20% testing data**.

Grid Search Cross Validation with **3 folds** was used for hyperparameter tuning.

The following machine learning models were trained:

- Logistic Regression
- Random Forest
- Gradient Boosting Trees
- Support Vector Machine
- Hybrid Model

---

## Model Performance

The **Logistic Regression model performed the best**.

Performance metrics:

- Accuracy: **0.92**
- F1 Score: **0.91**

These results indicate strong predictive capability for identifying potential churned users.

---

## Tools & Technologies

- Python
- Big Data Processing
- Apache Spark
- Machine Learning
- Feature Engineering
- Grid Search Cross Validation

---

## Key Insights

- User behavior patterns can effectively predict customer churn.
- Feature engineering from user activity logs significantly improves model performance.
- Machine learning models can help businesses proactively identify at-risk customers.

---

## Conclusion

This project demonstrates how large-scale user interaction data can be analyzed to predict customer churn. By identifying users who are likely to cancel their subscription, businesses can take targeted actions to improve customer retention and reduce revenue loss.

---

## Skills Demonstrated

- Big Data Analytics
- Feature Engineering
- Machine Learning Modeling
- Model Evaluation
- Hyperparameter Tuning
- Customer Churn Prediction
