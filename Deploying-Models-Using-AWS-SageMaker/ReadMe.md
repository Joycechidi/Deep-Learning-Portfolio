# Table of Content 
1. Introduction 
2.Installations
3. Description of files in this repo
4. Summary of steps taken in the project
5. Results
6. Licensing, Authors and Acknowledgement

## Introduction
Many data science students and scholars are stuck with the models they built and have no way of making it available for use to everyday people because the skills for deploying these models are rarely taught in most machine learning courses.

In this project, I used AWS SageMaker to Deploy an LSTM-based Sentiment Analysis of movie reviews. Created a simple web application where a user can enter a review and get back a response showing if their review or comments are either negative or negative.
I explained the steps taken to achieve this result.

## Installations
An AWS account is needed. THe free-tier account should be enough but I encountered a lot of permission errors so $100 AWS credit on a personal account worked well. This project needs more permissions than what an AWS educate account can provide.

pandas
torch
sagemaker_containers
pickle
json
argparse
os


## Description of files in this repo
1. train.py: A python script for the training algorithm
2. predict.py
3. model.py
4. index.html
5. SageMakerProject.ipynb

## Summary of steps taken in the project
1. Load the data for the project which is the movie reviews

2. Prepare and preprocess the data. To process the data, five major steps are taken
Get the texts out of the input review which could contatin hmtl tag so the tags are removed.
The texts are converted to lower case and all characters that are not alphabets nor digits with spaces.
Each word in the texts was split into a list and separated by space
All stopwords such as a, an, this, that, the, etc. were removed from the list
The words were then stemmed in the list which means converting words like eating/eat to eat.
A valid word dictionary was constructed.
3. Build and Train the PyTorch Model in the train.py script and the SageMakerProject.ipynb

4. An XGBoost model was also trained and then compared with the Rceurrent Neural Network(RNN) model. The RNN was trained using the SageMaker's supported PyTorch functionality.
5. **AWS SageMaker SetUp**, I created a notebook instance using a notebook type: __ml.p2.xlarge__
6. Chose the S3 bucket was set up in the notebook instance for training data and model artifacts.
7. I requested for an increase in the ml.p2.xlarge instance because the default value was zero.
8. Lambda function was created and the endpoint value from the training process was updated on the lambda function in SageMaker.
9. A RESTAPI was created in the AWS console to for the web application url. The created url was updated in the index.html file.

## Results
The model was deployed and the Lambda / API Gateway integration is complete so that the web app works (make sure to include your modified index.html).

## Licensing, Author and Acknowledgement
Project author: Joyce Chidiadi
Acknowledgement: Udacity code platform
