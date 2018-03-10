# Transfer Learning

This repo contains examples of [transfer learning](http://sebastianruder.com/transfer-learning/) using Keras and Tensorflow.

**Directory MNIST**: For this case, a CNN model is trained on the even digits of the MNIST data set.  After training, the feature detection layers of the CNN model are frozen and the model's classification layers are updated to recognize odd digits.


**Directory cats_dogs**: Illustrates transfer learning using a pre-trained Imagenet-based CNN model.