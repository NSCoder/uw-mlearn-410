# Instructions

Convolutional neural networks have a number of hyperparameters and architectural options. In these exercises you will investigate some of these options.

Construct the following three convolutional neural networks, all with early stopping:
1. A network that uses tiling of the convolutional operator:
    - 3 2-d convolutional layers with operator span of 2X2, stride of 2X2, reclilinear activation, and zero padding. 
    - The first 2 convolutional layers are to be followed by a max pooling layer with 2X2 operator. 
    - A flattening layer.
    - A dense hidden layer with 64 units, recliliner activation and l2 regularizaton with hyperparameter = 0.01. 
    - A dropout layer with p = 0.5. 
    - An output layer with 10 units and softmax activation.


2. A network that uses a convolutional operator with a larger span (Note this model will take a while to train):
    - 3 2-d convolutional layers with operator span of 5X5, reclilinear activation, and zero padding. 
    - The first 2 convolutional layers are to be followed by a max pooling layer with 2X2 operator. 
    - A flattening layer.
    - A dense hidden layer with 64 units, recliliner activation and l2 regularizaton with hyperparameter = 0.01. 
    - A dropout layer with p = 0.5. 
    - An output layer with 10 units and softmax activation.


3. A network with deeper covolutional layer:
    - 4 2-d convolutional layers with operator span of 3X3, reclilinear activation, and zero padding. 
    - The first 3 convolutional layers are to be followed by a max pooling layer with 2X2 operator. 
    - A flattening layer.
    - A dense hidden layer with 64 units, recliliner activation and l2 regularizaton with hyperparameter = 0.01. 
    - A dropout layer with p = 0.5. 
    - An output layer with 10 units and softmax activation.

For each of the above convolutional networks answer the following questions comparing each network with the second convolutional network in the lesson network (the networ with padding). This is the baseline network. 
1. How do the number of parmeters for the 2-d convolution layers compare to the 32 and 64 channel layers in the baseline network?
2. How does the number of parameters in fully connected hidden layer compare to that layer in the baseline network. 
3. How does the accuracy of the outcome compare to the baseline network?