# Stock-Market-Detection
Stock Market Prediction using deep learning
Predicting the stock price via Computers has been the motive of investors since the inception of Modern Technology. This thesis tries to look for the best model to predict the fluctuation in stock prices. It also tries to predict the stock movement with higher accuracy with a comparative study between LSTM(Long Short Term Memory) and GRU(Gated Recurrent Unit).

Concepts Used:
LSTM
The LSTM is made up of four neural networks and numerous memory blocks known as cells in a chain structure. A conventional LSTM unit consists of a cell, an input gate, an output gate, and a forget gate. The flow of information into and out of the cell is controlled by three gates, and the cell remembers values over arbitrary time intervals. The LSTM algorithm is well adapted to categorize, analyze, and predict time series of uncertain duration.
input Gate: It determines which of the input values should be used to change the memory. The sigmoid function determines whether to allow 0 or 1 values through. And the tanh function assigns weight to the data provided, determining their importance on a scale of -1 to 1.

Forget Gate: It finds the details that should be removed from the block. It is decided by a sigmoid function. For each number in the cell state Ct-1, it looks at the preceding state (ht-1) and the content input (Xt) and produces a number between 0 (omit this) and 1 (keep this).

Output Gate: The block’s input and memory are used to determine the output. The sigmoid function determines whether to allow 0 or 1 values through. And the tanh function determines which values are allowed to pass through 0, 1. And the tanh function assigns weight to the values provided, determining their relevance on a scale of -1 to 1 and multiplying it with the sigmoid output.


 
 
GRU
GRU ( Gated Recurrent Units ) are similar to the LSTM networks. GRU is a kind of newer version of RNN. However, there are some differences between GRU and LSTM.
GRU doesn’t contain a cell state
GRU uses its hidden states to transport information
It Contains only 2 gates(Reset and Update Gate)
GRU is faster than LSTM
GRU has a lesser tensor operation that makes it faster
1. Update Gate
Update Gate is a combination of Forget Gate and Input Gate. Forget gate decides what information to ignore and what information to add to memory.
2. Reset Gate
This Gate Resets the past information in order to get rid of gradient explosion. Reset Gate determines how much past information should be forgotten.


Result
The metric into account is the dataset of the exchange prices from the previous year. After pre-processing the data, we implemented LSTM and GRU algorithms on the dataset and compared the results it generated with metrics like r2, which is (total variance explained by the model) / (total variance).In addition, the thesis examines the limitations of these models and the issues associated with predicting stock prices.
By measuring the accuracy of both the models, we found that the optimal algorithm for predicting the value of the stock by the historical data is the GRU model.
The future scope of this project will involve adding more metrics and factors like financial ratios and public sentiment, as more parameters, improve the accuracy of the model and makes it much more realistic.

