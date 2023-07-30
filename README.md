# Stock Market Prediction with LSTM for Apple (AAPL) Stocks

This repository contains a simple implementation of a Long Short-Term Memory (LSTM) model for stock market prediction of Apple (AAPL) stocks. The code uses historical stock price data from the CSV file named "AAPL.csv" to train the LSTM model and make predictions on future stock prices.

## Code Overview

1. **Data Loading and Preprocessing:** The code reads the historical stock price data from the "AAPL.csv" file and preprocesses it. It converts the "Date" column to a datetime format and sets it as the DataFrame's index. The closing prices are plotted to visualize the data.

2. **Data Scaling:** The closing price data is scaled between 0 and 1 using MinMaxScaler from scikit-learn. Scaling is a common practice to normalize the data for neural network training.

3. **Prepare Training Data:** The code prepares the training data, creating sequences of 60 consecutive stock prices as input and the next stock price as the output. This step is essential for training the LSTM model to learn sequential patterns in the data.

4. **LSTM Model Building:** The LSTM model is constructed using Keras with two LSTM layers and one dense layer. The 'adam' optimizer and 'mean_squared_error' loss function are used for model compilation.

5. **Model Training:** The LSTM model is trained with the training data using one epoch and a batch size of 1.

6. **Test Data Preparation and Prediction:** Test data is prepared for predicting future stock prices. The trained LSTM model is then used to make predictions on the test data.

7. **Inverse Scaling of Predictions:** The predicted stock prices are inverse transformed to their original scale using the MinMaxScaler.

8. **Model Saving:** The trained LSTM model is saved as "saved_model.h5" for future use.

9. **Visualization:** The historical closing prices of AAPL stock (training data) and the predicted closing prices (validation data) are plotted on the same graph.

## Note

This implementation provides a basic demonstration of using LSTM for stock market prediction. However, predicting stock prices is a complex task influenced by numerous factors, and historical price data alone might not be sufficient to capture all the dynamics involved. For accurate and reliable predictions, more sophisticated models and additional features may be required.

Please exercise caution and perform a thorough evaluation before using any stock market prediction model for actual trading or investment decisions.

## Usage

To run the code, make sure you have Python, pandas, numpy, matplotlib, Keras, and scikit-learn installed. Also, place the "AAPL.csv" file in the same directory as the script. Then, execute the script, and the model will be trained and predictions will be made.

Feel free to experiment with the code and customize it as needed for your specific use case. Happy coding!
