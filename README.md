# Transfer Learning

This repo contains examples of [transfer learning](http://sebastianruder.com/transfer-learning/) using Keras and Tensorflow.

One example of transfer learning uses the MNIST handwritten digit dataset. For this case, a CNN model is trained on the even digits of the MNIST data set.  After training, the feature detection layers of the CNN model are frozen and the model's classification layers are updated to recognize odd digits.

