## Deep Learning ND First Project
In this project, I built a neural network which I used to predict daily bike rental ridership pattern.
The neural network is written in python.

I used only numpy without PyTorch or TensorFlow and all codes are written in python from scratch without any 3rd-party packages used. 

### Steps taken in the project
1. Load and Prepare the data
2. Visualize the data to get a good view of the first few entries
3. Take care of categorical variables such as season, weather, month, etc.
4. Scale the target variables
5. Split the data into training, testing and validation sets. Since this is a time-series data,, I'll train on historical data and then try to predict on future data which is the validataion data set.
6. Build the network with 2 layers (inout and output layer) where the hidden layer uses the sigmoid activation function and the output layer has only one nde which is used for regression.
For a little explanation, an activation function is a funtion that takes the input signal and generates an output signal, but takes into account the threshold. 

I worked through each layer of the network calculating the outputs for each neuron. All the outputs of one layer becomes the inputs to the neuron sof the next layer. This is called the forward propagation.

Then, a backprpagation is performed by using the weights to propagate the signals forward from the input to the output layers in a neural network. The weights are also used to propagate the errors backwards from the output back into the network to update the weights.
7. Perform a unit test to check whether the network built was correctly implemented.
8. Train the network: First, choose the hyperparameters that will ensure the lowest error on the training set and at the same time not overfit.
I used a Stochastic Gradient Descent(SGD) to train the network. Why? This is because I want to grab a random dample of the data for each training pass which provides more efficient trainingod the network.
Chose a reasonable number of hidden nodes.
9. After training, use the test data to see how well the trained network will model the data.
