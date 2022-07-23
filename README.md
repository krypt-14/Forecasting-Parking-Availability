# Forecasting Parking Availability Using LSTM Neural Network
#### Authors
- [Wei Jun Poh](https://github.com/krypt-14)

This project is based on my final year group thesis from University of Sydney, where my group have presented on the theme of Smart City and how different sustainable method such as parking are an efficient way to manage and control traffic as well as control the number of vehicle can take in certain areas. 

For the purposes of the topic, I am only demonstrating on how the model is preprocess and develop to provide future forecasting for parking availability. 

## Overview
The project revolves around smart parking availability system based on the data collected from sensors placed in the parking bays around Melbourne, Australia. It delves into building an end to end model that predicts parking availability with a high confidence. This is for 15 minutes interval timesteps based on the location of road segment, user destination, date and time. The project aims to ameliorate traffic congestion issues and provide efficiency, by giving users prefictable insights into future parking conditions through seasonality. 

The prediction model is based on the long short-term memory (LSTM) neural networks and has been implemented on Melbourne CBD on-street parking dataset that has been preprocessed and aggregated on Google's Big Query. We achieved a test Mean Absolute Error (MAE) of 0.1634 for the year of 2019, with a two-layer stacked LSTM on a 24 hour multi step output. The prediction results are filtered to display the user preferences captured via a user interface (UI) that was built on Flask and Mapbox. We present an end to end model built on cloud tools as the building blocks for future work in a wide array of applications. This includes creating insights and patterns based on the occupancy and restriction violation data of the parking lots, helping the city council in making data driven decisions and better planning for the future.

## System Architecture

![](https://github.com/krypt-14/Jun/blob/master/system_architecture.JPG)

### Step 1 - Preparing and Extrating Data
In summary this data is extract through City of Melbourne on-street parking dataset through connecting to their API, and was preprocess on Google CLoud Services. 

### Step 2 - Preparing the Model 
The subfolder "Model" will test out the accuracy score of the LSTM model to present the prediction on the dataset given through preprocessing

### Step 3 - Preparing the UI Interface
The user interface is built around flask and present the visualization of the result from the LSTM Model
