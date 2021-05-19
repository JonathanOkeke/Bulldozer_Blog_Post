# Bulldozer Sale Prices in the USA
## 0. Introduction
**In this mini Data Science project, I sought to develop a model that can predict the price of a Bulldozer today using historical data.**  
## 1. Problem Definition
**This analysis was approached from the point of view of a company wanting to sell it inventory of used bulldozers at auctions around the USA.**  

The analysis seeks to answer the following business questions:-  
### 1.1 Business Questions
#### 1.1.1 For bulldozers of similar age , usage and model type, is their sale price  dependant on where / what State the bulldozer is sold from ? If so , in which State can we expect to get the best price for our bulldozer ?
#### 1.1.2 What is the sale price variation across diffferent bulldozer models of the same age and usage ?
#### 1.1.3 What is the "best" time of the year to sell a bulldozer on average ?
### 1.2 Modelling Objective
#### 1.2.1 How much can we expect to get for the sale of a particular bulldozer ? Can we build a predictive model to determine what is the appropriate sale price of certain bulldozers ? 
> How well can my model predict the future sale price of a bulldozer, given certain characteristics, using historical data indicating how much similar bulldozers sold for.
## 2. Data
The data is downloaded from the "Kaggle Bluebook for Bulldozers Competition"

Link to the kaggle page : https://www.kaggle.com/c/bluebook-for-bulldozers/data   

The data for this competition is split into three parts:

* Train.csv is the training set, which contains data through the end of 2011.
* Valid.csv is the validation set, which contains data from January 1, 2012 - April 30, 2012 You make predictions on this set throughout the majority of the competition. Your score on this set is used to create the public leaderboard.
* Test.csv is the test set, which won't be released until the last week of the competition. It contains data from May 1, 2012 - November 2012.   

The key fields are in train.csv are:

* SalesID: the uniue identifier of the sale
* MachineID: the unique identifier of a machine.  A machine can be sold multiple times
* saleprice: what the machine sold for at auction (only provided in train.csv)
* saledate: the date of the sale  

The machine_appendix.csv file contains the correct year manufactured for a given machine along with the make, model, and product class details. There is one machine id for every machine in all the competition datasets (training, evaluation, etc.).  

**Refer to the data dictionary for more detialed descriptions of each feature in the aforementioned datasets.**  

**Link to the Data Dicitonary here** -> https://drive.google.com/file/d/137C96v4USPF__97pBNIJ1AaKBkJsOJuB/view?usp=sharing

## 3. Evaluation

The evaluation metrics used for determining the accauracy and reliability of the sale price predictive model will be  the `MAE` **(Mean Absolute Error)** between the actual and the predicted auction sale prices and the `R^2 score`.

### Goal
- **Minimise the RMSLE**
- **Maximise the R^2 score**
## 4. Answering the Business Questions
### 4.1 For bulldozers of similar age , usage and model type, is their sale price  dependant on where / what State the bulldozer is sold from ? If so , in which State can we expect to get the best price for our bulldozer ?  
The analysis of the mean sale price for each bulldozer type revealed that:  

- Generally speaking, it would be more advisable for the company to sell their bulldozers in **North Dakota**. This is beacuase **bulldozers sell for a higher price , on average in North Dakota**.  

- **For Motor Graders**: The best state to sell in is **South Dakota**.
- **For Wheel Loaders**: The best state to sell in is **Rhode Island**.
- **For Tractors**: The best state to sell in is **Nevada**.
- **For Excavators**: The best state to sell in is **North Dakota**.
- **For Backhoe Loaders**: The best state to sell in is **South Dakota**.
- **For Skid Steer Loaders**: The best state to sell in is **Rhode Island**.
