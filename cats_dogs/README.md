# Cats and Dogs Image Classification

This use case using transfer learning to classify whether an image is one of a cat or a dog.  Data for this work comes from the [Kaggle Cats and Dogs Redux competition](https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition).  The techniques shown in this work is based discussions found in [Deep Learning with Python](https://www.manning.com/books/deep-learning-with-python) by F. Chollet.  [Companion software](https://github.com/fchollet/deep-learning-with-python-notebooks) for the book is located at github.com

Note: Results shown in the book and github repo for the VGG16 transfer example are incorrect.  According to this [posting](https://github.com/keras-team/keras/issues/8792) there was a bug in Keras releases prior to 2.1.  This bug allowed weights in the pre-trained model to be updated when they should have been frozen.  The validation accuracy shown in this repo are correct.

Unless noted otherwise, all notebooks were run on an AWS p2.xlarge instance, which provides an Nvidia K80 GPU. [Amazon Deep Learning (Ubuntu) AMI](https://aws.amazon.com/marketplace/pp/B077GCH38C) provided the deep learning software stack.

|Notebook|Deep Learning Software Stack|
|--------|-----------|
|[prepare_train_validation_test_data.ipynb](https://github.com/jimthompson5802/transfer_learning/blob/master/cats_dogs/prepare_train_validation_test_data.ipynb)|Creates training, validation and test data sets.|
|[vgg16_small_transfer_learning.ipynb](https://github.com/jimthompson5802/transfer_learning/blob/master/cats_dogs/vgg16_small_transfer_learning.ipynb)|Keras front-end api with Tensorflow backend.  Transfer learning using pre-trained VGG16 imagenet model.  Illustrates both feature extraction and fine-tuning using only 4,000 images for training. __Achieved 0.9665 accuracy on out-of-sample test set__.|
|[vgg16_full_transfer_learning.ipynb](https://github.com/jimthompson5802/transfer_learning/blob/master/cats_dogs/vgg16_full_transfer_learning.ipynb)|Keras front-end api with Tensorflow backend.  Transfer learning using pre-trained VGG16 imagenet model.  Illustrates both feature extraction and fine-tuning using 21,000 images for training. Achieved 0.9765 accuracy on out-of-sample test set.|
|[vgg16_full_transfer_learning_multi-gpu.ipynb](https://github.com/jimthompson5802/transfer_learning/blob/master/cats_dogs/vgg16_full_transfer_learning_multi-gpu.ipynb)|Keras front-end api with Tensorflow backend.  Demonstrates multi-gpu training. Tested on AWS p2.8xlarge instance with 8 Nvidia K80 gpus.  Performance impact of multi-gpu training is shown [here](https://github.com/jimthompson5802/transfer_learning/wiki). Encountered one issue: ModelChekcpoint call-back to save best weights did not work in muti-gpu mode. Disabled that call-back. More research needed to see how this could work with multiple gpus.  See issues [#9548](https://github.com/keras-team/keras/issues/9548) and [#8764](https://github.com/keras-team/keras/issues/8764).|


**High-level Transfer Learning Steps**

* Extract pre-trained model structure (convolution and maxpool layers) and weights, excluding the original top-level classicfication fully connected layers.

* Add new top-level fully connected layers for cat vs dog classification.

* Freeze weights in the pre-trained model

* Using the pre-trained layers and frozen weight for feature extraction, train the new top-level for cat vs dog classification. Data augmentation is used to minimize overfitting. During training save weights for best performing model on validattion data set.

* Save model structure and best performing weights.

* Report accuracy of trained model on out-of-sample test data set.

* Fine tune current model by unfreezing selected upper layers of the pre-trained layers and continue training.  Data augmentation is used to minimize overfitting.  During training save weights for best performing model on validattion data set.

* Save model structure and best performing weights.

* Report accuracy of trained model on out-of-sample test data set.



