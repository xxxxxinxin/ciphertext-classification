# ciphertext-classification

### Method Name ###
cipherword word2vec + BiLSTM

### Representation of sentence ###
Trained a word2vec model on all sentences from scratch and use the model to get the representation of each word.

### Classifier ###
The encoder is LSTM without pre-training. One dropout layer is added to avoid overfitting. And implemented sigmoid function to do classification. The loss function is binary cross entropy, which is used to know whether the model do the right prediction and can be used as learning objective.


### Training & Development ###
Evaluated the solution by using the trained model to predict the dev set and compare the result with the label given in the set. Some key hyper parameter: optimizer = Adam optimizer; learning rate=0.001; batch size = 64. Terminated the training with a fixed epoch, which is decided based on 