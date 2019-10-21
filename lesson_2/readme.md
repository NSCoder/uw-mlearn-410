# Instructions
Changes in both architecture and regularizaiton have significant effects on the training behavior or neural networks. In this exercise, you will explore changes in training behavior with architecture and regularization.

Using the models for classifing the MNIST digits in the *Getting Started with Keras* notebook, create the following neural networks and answer the questions below about each.

1. A network with a single hidden layer of 1024 units. Compare these results to the single layer model with 512 units. 
2. A network with 2 hidden layers of 1024 units, using L2 kernel regularizaiton with parameter 0.01. Compare these results to the single hidden layer network with 1024 units. 
3. A network with 2 hidden layers of 512 units, using L2 kernel regularizaiton with parameter 0.01. Compare the results to a) the single hidden layer network with 512 units and L2 regularization, and b) the 2 hidden layer network with 1024 units with L2 regularization. 
4. A network with 4 hidden layer of 512 units, using L2 kernel regularizaiton with parameter 0.01. Compare the results to a) The two hidden layer network with 512 units per layer and L2 reegularization, and b) the 2 hiddent layer network with 1024 units per layer and L2 regularization.

For each of these networks create charts showing training error and test error vs. epoch, and training loss vs. testing loss vs. epoch. Based on your observations from these charts and your knowledge of neural networks, answer the following quesitons. Comparisons should be made to other networks as specified above.

1. How do the number of training epochs before over-fitting compare?
2. How does the best loss function compare? 
3. How does the best accuracy metric compare?

Note: As you proceed you should consider how the  capacities of these models differ and what regularization steps might give better results. 