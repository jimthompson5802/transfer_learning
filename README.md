# Transfer Learning

This repo contains examples of [transfer learning](http://sebastianruder.com/transfer-learning/) using various Python Deep Learning packages.  

A CNN model is trained on the even digits of the MNIST data set.  After training the feature detection layers of the 
CNN model are frozen and the model's classification layers are updated to recognize odd digits.

|Notebook|Deep Learning Software Stack|
|--------|-----------|
|[transfer_learning_example](https://github.com/jimthompson5802/transfer_learning/blob/master/transfer_learning_example.ipynb)|Keras and Theano|
|[transfer_learning_example_tf_keras](https://github.com/jimthompson5802/transfer_learning/blob/master/transfer_learning_example_tf_keras.ipynb)| TensorFlow with Keras Layer API|

