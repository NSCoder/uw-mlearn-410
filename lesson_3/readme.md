# Instructions
## Regularization methods

A number of regularization methods are commonly used for training deep neural networks. A major issue in applying regularizaiton methods is the bias-variance trade-off. Regularization methods reduce the variance of the model, and improves generalization. Unfortunately, added bias is the price paid for using regularization to reduce variance. There is a two-fold challenge when applying regularizaiton:

1. Find the combination of regularization methods that best fits the problem. In most cases, early stopping is a given, but there are other choices which must be made.
2. For any combination of regularizaton methods the parameters must be chosen to minimize test errors and loss.

In this exercise you will implement and compare the following regularization methods on the MNIST data set classification problem. In each case you will use a neural network with 4 hiden layeres and 512 units per layer and rectilinear activation function. Apply automated early stopping.

1. A neural network using only l2 regularization with regularization parameters 0.01, 0.02, 0.03, 0.04, 0.05. 
2. A neural network using l2 regularization with parameter 0.01 and dropout regularization with p = 0.3, 0.4, 0.5, 0.6, 0.7. 
3. A neural network using dropout regularization with parameter 0.5 and l2 regularization with parameters 0.002, 0.004, 0.006, 0.008, 0.01.

For each of these cases do the following:
1. Create plots of both the training accuracy and training loss vs. the regularization parameter.
2. Deterimine which parameter setting is most effective. 
3. Is this regularization method superior to the other or not.

**Hints:** 
1. For the early stopping using the following settings:
- patience = 1
- monitor = 'val_loss'
2. Expect the interpretation to somewhat confounded by possible run-to-run variation in the test statistics. If you desire a greater challenge you can compute more reliable statistics by using k-fold cross-validation with some reasonable k. 
3. Use a batch size of 512 to speed up model training.