# Credit Card Fraud Detection App built with Streamlit, FastAPI and Docker
An end-to-end Machine Learning Project  to detect fraudulent credit card transactions. Built with FastAPI, Streamlit and Docker.

## Problem Statement
Credit card fraud is an inclusive term for fraud committed using a payment card, such as a credit card or debit card. The purpose may be to obtain goods or services or to make payment to another account, which is controlled by a criminal.
 
**This Streamlit App utilizes a Machine Learning model served as an API with FastAPI framework in order to detect fraudulent credit card transactions  based on the following criteria: hours, type of transaction, amount, balance before and after transaction etc.**

The machine learning model used for this web application was deployed as an API using the FastAPI framework and then accessed through a frontend interface with Streamlit.


## Data Preparation
A synthetic dataset generated using the simulator called PaySim was used as the dataset for building the  project. PaySim uses aggregated data from the private dataset to generate a synthetic dataset that resembles the normal operation of transactions and injects malicious behaviour to later evaluate the performance of fraud detection methods.

[Dataset Link](https://www.kaggle.com/datasets/ealaxi/paysim1v)

### Modelling
In this project 2 different classification algorithms were tested namely:

- Logistic Regression
- Random Forest

The final model used for the API was the **Random Forest Classifier** model which had an accuracy score of 0.99 and an F1 score of 0.86.


## Preview

### API Demo
![api](https://user-images.githubusercontent.com/101701760/174500152-c6256170-5c8e-42dd-b5e7-4a01c805ab99.gif)


### Streamlit App Demo


![credit](https://user-images.githubusercontent.com/101701760/174500101-d70e5ec1-bb50-4a67-be13-1cb561c9ed11.gif)


                    User                                                                            
                      │
                      ▼
            Browser (localhost:8501)
                      │
                      ▼
          Streamlit Container
                      │
          HTTP POST /predict
                      │
                      ▼
            FastAPI Container
                      │
              model.pkl
                      │
                      ▼
          Random Forest Model
                      │
                      ▼
             Prediction Result
                      │
                      ▼
          Streamlit Container
                      │
                      ▼
                 User





