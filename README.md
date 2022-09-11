# Syma - RecSys 2022 Challenge [![Profile][title-img]][profile]

[title-img]:https://img.shields.io/badge/-SCIA--PRIME-red
[profile]:https://github.com/Pypearl

## Objective

The objective of the project is to improve a **recommendation system** with application to the **dressipi challenge**. The goal was to obtain the best possible score on the online challenge, and to try different way to have a good score. The notebook go through our **analysis** of the data, then on the different process and **alteration** that we have done to produce our final dataset, and finally on our different **machine learning** technique to generate our submissions.

## Dataset

For this challenge we had access to multiple datasets that gave us many information about the behaviour of the customers. 

There were 5 datasets :
* `candidate_items.csv`: contains all the items available
* `item_features.csv`: contains all the features of each item
* `train_purchases.csv`: contains all the purchases that occurred at the end of a session.
* `train_sessions.csv`: contains all the items viewed in a session for each
session_id
* `test_leaderboard_sessions`: contains the input sessions for the leader-board

## Data pre-processing

After this analyse, we had to **pre-process** the data in order to use them in our recommendation system. The items used 73 category of features. Even if 73 category is not a lot, it is still a big number and we had to reduce the dimension of our data to apply ML algorithm later. 

We used a **truncated SVD** to reduce our items **sparse matrix** to 12 components. This matrix allowed us to find easily and faster the **embedding items** of each items. We had just to compare the value of their components in the matrix

## Machine Learning
For the machine learning part, we used two different models to generate our
submission. The first one is a logistic regression and the second one is a simple
RNN (Recursive Neural Network).
When evaluating the models on a test dataset, the logistic regression gave us a
decent accuracy score of 79,99% , whereas the RNN gave us a quite better score
of 80,91%.

<img src="https://github.com/Pypearl/PTML/blob/main/readme_images/supervised_vis.png" alt="Supervised_Visualization">

