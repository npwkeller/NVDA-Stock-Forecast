# NVDA-Stock-Forecast

The goal of this project was to get some hands on experience in Python within the field of Finance. To do this I wanted to attempt the age old task of predicting stock prices, specifically by using only historical data, and not considering fundamental analysis or other influencing factors such as the news. I began by extracting data from yfinance, then I did some basic data exploration and visualization using matplotlib, seaborn, and plotly. Looking at NVDA histogram of returns and beta, I found NVDA stock is more volatile then the market, especially im recent times because of this I waned to continue to use the 2y time frame of data as I believe it accurately represents some of the current volatility in the market in our post covid-19 environemnt. 

Now I was ready to train the model, first it was important to scale the data, then I made a function to create the lag variables which would be our training variables where t-l would be used to predict t. Then I created the sequential LSTM model which allows me to stack multiple layers including two LSTM layers to process the input sequences, two dropout layers to avoid overfitting, and two dense layers to capture relationships and output the results.

Once the model was created, I turned it into a function to easily fine tune the hyperparameters, explored residual statisitcs, and visualized our results against the test data and created residual plots.

The model performed very well with an RMSE of $15.53 and r^2 of .958 but looking at the residuals it had a strong bias towards underpredicting the stock price. 

Moving forward, I would like to further experiment with the hyperparamters and layer set up of the model. Adjusting things such as neurons, batch size, dropout, etc..

Let me know if you have any comments or feedback. I can be reach at npwkeller@gmail.com or https://www.linkedin.com/in/ian-keller-31a86719a/
