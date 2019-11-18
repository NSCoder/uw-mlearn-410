Assignment 6

Working with text sequences

Part 1.
In the last lesson we examined using recurrent neural network (RNN) models for text analysis. Specifically, various RNN architectures were applied to classification of sentiment in the IMDB movie reviews. A similar analysis can be performed using convolution neural network (CNN) architectures. To explore this idea build and examine the results from the following two models.

First construct and test the following CNN:   
1. Pad the input text strings to a maximum length of 250.         
2. Use an Embedding input layer with max_features = 10000, output_dim = 32, and input_length = 250.     
3. A Conv1D layer with 32 channels and span of 3.    
4. A MaxPooling1D layer with pool_size=2.    
5. Another Conv1D layer 64 channels and a span of 3.    
6. A Flatten layer.     
7. A Dense binary output layer with activation = 'sigmoid'.     
8. For the optimizer use 'RMSprop' with loss = 'binary_crossentropy', and metrics = ['acc'].    
9. Fit the model with 10 epochs, and batch_size = 256.   

Perform the same experiment but add l2 regularization (kernel_regularizer = regularizers.l2(0.005)) to the Conv1D layers.

Part 2.
Early stopping is a powerful regularization method. Early stopping can be one of the best ways to prevent over-fitting in any machine learning model, including neural network models. In this exercise you will apply early stopping to a gated recurrent unit (GRU) as follows:

1. For the EarlyStopping callback use a) monitor = 'val_loss', and b) patience = 1. Notice that this is different from all previous examples which used patiencec = 1. For the ModelCheckpoint call back, set your file path and a) use monitor = 'val_loss', and b) save_best_only = True.
2. Pad the input text strings to a maximum length of 250. 
3. Use an Embedding input layer with max_features = 10000, output_dim = 32, and input_length = 250.
4. A GRU layer with 32 hidden units, and kernel_regularizer = regularizers.l2(0.005).
5. A Dense binary output layer with activation = 'sigmoid'.
6. For the optimizer use 'RMSprop' with loss = 'binary_crossentropy', and metrics = ['acc'].
7. Fit the model with 15 epochs (early stopping should ocur first), and batch_size = 256.

Questions to answer:

For both Part 1 and Part 2 above answer the following questions. 
1. How does the complexity of these networks, in terms of parameters, compare to the bidirectional GRU network in the lesson notebook. 
2. Is the performance in terms of accuracy and loss better, worse or about the same when compaired the GRU network in the lesson notebook?