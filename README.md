# Loan default predictor

</br>

A neural network coded from scratch, inclduing Stochastic Gradient Descent with both forward and backward propagation implemented from scratch.

The network is then applied to a variety of tasks, including the MNIST data set (

</br>

## To Use

1. Create an `archive` folder.
2. Download the following data sets:
  - [MNIST dataset](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv/)
  - [Loan approval dataset](https://www.kaggle.com/datasets/bhavikjikadara/loan-status-prediction)
  - [Loan default dataset (small)](https://www.kaggle.com/datasets/kmldas/loan-default-prediction)
  - [Loan default dataset (large)](https://www.kaggle.com/datasets/nikhil1e9/loan-default)
3. Extract the contents of each of the data sets directly into `archive` folder.
4. Run the notebook.

</br>

## Analysis of results

### MNIST
The network learns quickly, quickly decreasing loss and increasing accuracy in the first epoch. However, there is still a significant amount of variation in the loss and accuracy even after 10 epochs. I was able to get a consistent result on the test set of around 93% accuracy. This could perhaps be improved by adjusting parameters like learning rate and decay.

### Loan approval
There are very few data entries to go on, so the network is perhaps overfitting to the training set sometimes. As a result, the accuracies achieved in the test set varied hugely, between 70% and 97% in my experience. More data would significantly improve the consistency.

### Loan default (small)
There is 10000 entries of data but only 3 datapoints for each column, meaning this model is highly unrealistic for any real world use. However, as a result of these properties, I was able to achieve around 96% accuracy on the test set consistently.

### Loan default (large)
There are over 250000 data entries, each with 16 data points, allowing the network a high number of entries in the training set to finetune the weights. With a training set of 200000 entries, I am able to achieve 89% accuracy consistently on a test set of 10000 entries. This could perhaps be improved by adjusting learning rate, decay, and the number of neurons in hidden layers.

</br>

## Sources

The maths behind backpropagation: [3Blue1Brown](https://www.youtube.com/watch?v=tIeHLnjs5U8)

Learning decay: [GeeksForGeeks](https://www.geeksforgeeks.org/learning-rate-decay/)

Batches and epochs: [GreenCode](https://www.youtube.com/watch?v=cAkMcPfY_Ns)

Calculating accuracy: [Samson Zhang](https://www.youtube.com/watch?v=w8yWXqWQYmU)

