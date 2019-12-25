## Deep Learning ND First Project
In this project, I built a neural network which I used to predict daily bike rental ridership pattern.
The neural network is written in python.

I used only numpy without PyTorch or TensorFlow and all codes are written in python from scratch without any 3rd-party packages used. 

### Steps taken in the project
1. Load and Prepare the data

2. Visualize the data to get a good view of the first few entries.

3. Take care of categorical variables such as season, weather, month, etc.

4. Scale the target variables

5. Split the data into training, testing and validation sets. Since this is a time-series data,, I'll train on historical data and then try to predict on future data which is the validataion data set.

6. Build the network with 2 layers (input and output layer) where the hidden layer uses the sigmoid activation function and the output layer has only one nde which is used for regression.
For a little explanation, an activation function is a funtion that takes the input signal and generates an output signal, but takes into account the threshold. I worked through each layer of the network calculating the outputs for each neuron. All the outputs of one layer becomes the inputs to the neuron sof the next layer. This is called the forward propagation. Then, a backprpagation is performed by using the weights to propagate the signals forward from the input to the output layers in a neural network. The weights are also used to propagate the errors backwards from the output back into the network to update the weights.

7. Perform a unit test to check whether the network built was correctly implemented.

8. Train the network: First, choose the hyperparameters that will ensure the lowest error on the training set and at the same time not overfit. I used a Stochastic Gradient Descent(SGD) to train the network. Why? This is because I want to grab a random dample of the data for each training pass which provides more efficient trainingod the network.
Chose a reasonable number of hidden nodes. I changed the learning rate, number of hidden nodes for more than 32 times in different combinations before arriving at this model. Not the best way to do this but I needed to try different iterations for better model.

9. After training, use the test data to see how well the trained network will model the data.

### Prediction Result
First, the model performed very well in predicting the data from December 11 to December 21. The model started a sporadic unreliable prediction (overfitting) from December 22 to December 31 when there was low usage of the bikes.

### Explanation for the model performance
An explanation as to why the december holiday season predictions performing poor is because rior information about such trends was not captured in the data, i.e the dataset that we trained on does not have information on holiday season even for the previous year. 
So when a new pattern is experienced the model performance is bad. This can be solved by training the model with more data, possibly, randomised data so that the model captures such patterns and predicts well. 
If you are the manager for the bike sharing service, this is your first year int he company and you know about the trends from January to October, having a knowedge of this data trend, you are most likely to anticipate that the trends from your previous experience will hold right? 
So you would make preparations accordingly, but once december hits the holiday starts and then people stay at home. This could cause a slump which is the same case with this model. You will have this in mind the next year December right? If you notice properly the holiday season extends over a week, but you will find that the days near christmas which are considered holiday season are marked as non-holidays, so a new feature marking the holiday season will be really helpful along with training over additional holiday season data.

