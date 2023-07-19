# Handwritten-Digit-Recognition-Using-Multi-Layer-Perceptron
project to develop and train a deep multi-layered perceptron (MLP) to classify hand-written digits from the MNIST dataset.

Dataset
To download the MNIST dataset, follow these steps:
* 		Go to http://yann.lecun.com/exdb/mnist/.
    * Download all four files:
    * 'train-images-idx3-ubyte.gz'
    * 'train-labels-idx1-ubyte.gz'
    * 't10k-labels-idx1-ubyte.gz'
    * 't10k-images-idx3-ubyte.gz'
Place these downloaded files in a directory named 'DATA/MNIST'.


Model Architecture
The MLP model consists of input, hidden, and output layers.
* Input Layer: The input samples are grayscale images of size 28x28 pixels. Therefore, the shape of each training sample is (28, 28). The MLP expects the input samples to be flattened, resulting in a shape of (784,) for each input sample.
* Hidden Layers: The number of hidden layers and the number of neurons in each layer can be defined based on the architecture's design. For example, a common architecture could have 2 hidden layers with 256 neurons each.
* Output Layer: The output layer consists of 10 neurons, corresponding to the 10 possible classes (digits 0 to 9).
Activation Function
A common choice for the activation function in the hidden layers of the MLP is the Rectified Linear Unit (ReLU) function:
ReLU(x) = max(0, x)
Loss Function
For multi-class classification tasks like this one, the Cross-Entropy Loss function is commonly used:
Cross-Entropy Loss = -∑(y * log(y_pred))
where 'y' is the true label (one-hot encoded) and 'y_pred' is the predicted probability distribution over classes.
Optimization
The model parameters are updated using mini-batch stochastic gradient descent (SGD). In each iteration, a mini-batch of training samples is used to calculate the gradients and update the model's parameters.
Splitting Ratio
The training set is used to train the model, while the test set is used to evaluate its performance. A common splitting ratio is 80% for training and 20% for testing.
Plotting Loss and Accuracy
During the training process, the loss and accuracy are monitored after each epoch. The loss and accuracy plots are generated to visualize the model's performance on both the training and testing sets across different epochs.
