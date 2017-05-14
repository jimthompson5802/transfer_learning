# Transfer Learning

This repo contains a jupyter notebook illustrating transfer learning.  Using the Keras and Theano packages, a CNN model 
is trained on the even digits of the MNIST data set.  After training the feature detection layers of the CNN model
are frozen and the model is then trained on the odd digits to update the classification layer of the CNN model.
