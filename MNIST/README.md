# Transfer Learning

This repo contains examples of [transfer learning](http://sebastianruder.com/transfer-learning/) using various Python Deep Learning packages.  

A CNN model is trained on the even digits of the MNIST data set.  After training, the feature detection layers of the 
CNN model are frozen and the model's classification layers are updated to recognize odd digits.

|Notebook|Deep Learning Software Stack|
|--------|-----------|
|[MNIST/transfer_learning_example_keras_tf](https://github.com/jimthompson5802/transfer_learning/blob/master/MNIST/transfer_learning_example_keras_tf.ipynb)|Keras front-end with Tensorflow computational back-end|
|[MNIST/transfer_learning_example_keras_th](https://github.com/jimthompson5802/transfer_learning/blob/master/MNIST/transfer_learning_example_keras_th.ipynb)|Keras front-end with Theano computational back-end|
|[MNIST/transfer_learning_example_tf_keras](https://github.com/jimthompson5802/transfer_learning/blob/master/MNIST/transfer_learning_example_tf_keras.ipynb)| TensorFlow with Keras Layer API|
|[MNIST/transfer_learning_example_tf_keras_restore_only](https://github.com/jimthompson5802/transfer_learning/blob/master/MNIST/transfer_learning_example_tf_keras_restore_only.ipynb)|TensorFlow with Keras Layer API. Model restore and re-training only.|
|[MNIST/transfer_learning_example_tf_contrib_keras](https://github.com/jimthompson5802/transfer_learning/blob/master/MNIST/transfer_learning_example_tf_contrib_keras.ipynb)| TensorFlow based on tf.contrib.keras api set|
|[MNIST/transfer_learning_example_tf_contrib_keras_restore_only](https://github.com/jimthompson5802/transfer_learning/blob/master/MNIST/transfer_learning_example_tf_contrib_keras_restore_only.ipynb)|TensorFlow based on tf.contrib.keras api set. Model restore and re-training only.|
