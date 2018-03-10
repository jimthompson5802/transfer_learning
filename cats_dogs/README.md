# Cats and Dogs Image Classification

This use case using transfer learning to classify whether an image is one of a cat or a dog.  Data for this work comes from the [Kaggle Cats and Dogs Redux competition](https://www.kaggle.com/c/dogs-vs-cats-redux-kernels-edition).  The techniques shown in this work is based discussions found in [Deep Learning with Python](https://www.manning.com/books/deep-learning-with-python) by F. Chollet.  [Campanion software](https://github.com/fchollet/deep-learning-with-python-notebooks) for the book is located at github.com

Note: Results shown in the book and github repo for the VGG16 transfer example are incorrect.  According to this [posting](https://github.com/keras-team/keras/issues/8792) there was a bug in releases before Keras 2.1.  This bug allowed weights in the pre-trained model to be updated when they would have been frozen.  The validation accuracy shown in this repo are correct.

|Notebook|Deep Learning Software Stack|
|--------|-----------|
|[prepare_train_validation_test_data.ipynb](https://github.com/jimthompson5802/transfer_learning/blob/master/cats_dogs/prepare_train_validation_test_data.ipynb)|Creates training, validation and test data sets.|
|[vgg16_small_transfer_learning.ipynb](https://github.com/jimthompson5802/transfer_learning/blob/master/cats_dogs/vgg16_small_transfer_learning.ipynb)|Keras front-end api with Tensorflow backend.  Transfer learning using pre-trained VGG16 imagenet model.  Illustrates both feature extraction and fine-tuning using only 4,000 images for training. |



