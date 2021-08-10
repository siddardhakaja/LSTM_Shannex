# LSTM_Shannex

Predicting aggression level of a person after one week in a long term facility care. Dataset is private and cannot be shared.
Data is collected by Shannex and shared with AIDA for machine learning insights.



## Data Cleaning
provided data is cleaned for any non-ascii charecters or any stop words. 

## Data Manipulation
Since all the columns are nominal. Label encoding is applied and then one-hot encoding. The data is converted to a series from t-1 to t+5. Then the data is split into training and testing. Training dataset has 60 patients data and testing dataset has 15 patients data.

## Builing the LSTM Model

LSTM model has one LSTM layer with 128 units followed by  dropout layer and then dense layer with 100 units. Anther dropout layer, and dropout layer is added. The output layer is a dense layer with 4 units as show in the figure below.

Model: "sequential_2"
_________________________________________________________________
Layer (type)                 Output Shape              Param 

=================================================================
lstm_1 (LSTM)                (None, 128)               3560448   
_________________________________________________________________
dropout_3 (Dropout)          (None, 128)               0         
_________________________________________________________________
dense_3 (Dense)              (None, 100)               12900     
_________________________________________________________________
dropout_4 (Dropout)          (None, 100)               0         
_________________________________________________________________
dense_4 (Dense)              (None, 50)                5050      
_________________________________________________________________
dropout_5 (Dropout)          (None, 50)                0         
_________________________________________________________________
dense_5 (Dense)              (None, 4)                 204      

=================================================================

