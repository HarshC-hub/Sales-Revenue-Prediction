# Sales-Revenue-Prediction
LSTM model to predict sales revenue of any company / organisation
The goal of this project is to be able to estimate future sales of any firm, which will have a significant impact on the company's profit.
Secondly, it can be used to make plans. By looking at forecasts, we can plan our demand and supply operations. It aids in determining where additional investment should be made.
The biggest challenge in this project was deciding which model to use for training and testing. We tried CNN initially, but it produced a lot of errors. Next, we tried to forecast the model using a typical feed forward neural network, but the model's accuracy was far too low.
 We then tried using the LSTM (Long Short-Term Memory) model instead of CNN/ANN, which solved our problems.
The implementation of our model will require 3 basic steps:
1. Data wrangling - that is to purify or clean the data for our model to access it easily 
2. Data transformation - to forecast the sales more accurately and easily (i.e without any errors) we will do: -
	Check whether the data is stationary or not that is to check whether our data is constant or not and if it has any increasing or decreasing trend then we have to make it constant by creating another data frame.

	Then finally our data is a time series data therefore for LSTM model we'll be needing our feature set to be supervised therefore the conversion of time series to supervised data is necessary.
3. Lastly the data scaling that is to normalize our data for training and testing.

Here we used supervised machine learning training.
LSTM can be used both as supervised (classification, sequence prediction) and unsupervised (autoencoder) algorithm depending upon what loss function it optimizing looks like.
In this project we are using supervised learning for training our LSTM model.
Now the main motive to use the LSTM model is because in CNN / any other models it is challenging to use sequenced data because it is difficult to extract features suitable for us as input to supervised learning model.
Our task is to forecast monthly sales. We need to aggregate our data at monthly level and then sum up the sales column this will give us the sales at monthly level. 
Then we plotted the data to check whether it has any increasing or a decreasing trend. 
After plotting it shows that our data is not stationary (constant).
Now to make our data stationary we did try some trial-and-error methods. The one which gave us the solution we needed, was to get the difference between the current sales and the previous sales i.e of the previous month.
