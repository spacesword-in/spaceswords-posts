title: Starting with CNNs and Deep learning competitions
author: Kartik Verma
tags: []
categories:
  - AI 
  - Mini Project
date: 2017-11-09 12:27:00
---
<img src="https://github.com/convosyn/blogs/blob/master/blog1/DigitRecognitionCNNImageMain.png?raw=true" width="360" height="270">

Convolution neural networks are the state of the art deep learning algorithms in computer vision that have performed exceptionally well in the recent years and are able to achieve very high accuracy on the __imagenet__ challenge. Not only this they have also outperformed the humans in recognizing the images accurately.

In this tutorial we will use kaggle digit recognition dataset as our main dataset for training and will achieve an accuracy of greater than 95% and learn how to do it in python using well established libraries.
we will use **keras** to create our cnn model.

# Overview
In this tutorial we will learn the following: 
1. Dowloading the dataset
2. Loading the dataset
3. Creating the CNN model
4. Training the model
5. Evaluting the model
6. Saving the predictions

## Downloading the dataset
First we will download the [dataset](https://www.kaggle.com/c/digit-recognizer/data) from the kaggle site. Save the downloaded files in folder.
Open the files and see what you can understand.

## Loading the dataset

```shell
#Change to the directory in which the dataset is stored
$ cd ./digitRec 
```
Our CNN model will take (1, 28, 28) images as input so we load the images and reshape them to (1, 28, 28).
```python
#load the required modules
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import matplotlib.image as imgplt
from keras import backend as K

#set the image dimesion ordering channels first or channels last
#use 'th' for channels first 
K.set_image_dim_ordering('th')
def ld():
"""
	load the train and test files and return them as 4D array
"""
	file_train, file_test = 'train.csv', 'test.csv'
	train, test = np.array(pd.read_csv(file_train), dtype='float64'), np.array(pd.read_csv(file_test), dtype='float64')
	sp_train = train.shape[0]
	sp_test = test.shape[0]
	Xtrain, Ytrain, Xtest = train[:, 1:], train[:, 0], test
	Xtrain, Xtest = Xtrain.reshape(sp_train, 1, 28, 28), Xtest.reshape(sp_test, 1, 28, 28)
	print("testing data set image: ")
	img1 = Xtrain[0].reshape(28, 28)
	img2 = Xtest[0].reshape(28, 28)
	plt.subplot(2, 1, 1)
	plt.imshow(img1)
	plt.subplot(2, 1, 2)
	plt.imshow(img2)
	plt.show()
	return Xtrain, Ytrain, Xtest
```
save this script in file: loadDataSet.py

## Creating the model
Let's start with creating a cnn model. 


Filters are the layers of a convolutional layer that have been found to detect edges and other general features like orientation, colors, shapes etc.


our model will use 5 convolutional layers with different filter count.Usually the number of filters increase as we go deep in a network and the size of the layer decreases.


Let's start coding:
```python
import numpy as np
from keras.models import Sequential, Model
from keras.layers import Dense
from keras.layers import Dropout
from keras.layers import Flatten, Input, Add
from keras.layers.convolutional import Conv2D
from keras.layers.convolutional import MaxPooling2D
from keras.utils import np_utils
from keras import backend as K
from keras.constraints import maxnorm
from keras.optimizers import SGD
from sklearn.model_selection import train_test_split
import loadDataSet
import keras.layers
import pandas as pd
seed = 11
np.random.seed(seed)
```
Use a constant seed value so that the model and weights can be recreated.
Lets use our previous script 'loadDataSet.py' to load the files. 
```python
print("loading dataset")
Xtrain, Ytrain, Xtest = loadDataSet.ld()
```
We can do some preprocessing.

Let's center the data about the mean.
this will ensure that our model does not overfit.
```python
Xtrain_mean = Xtrain.mean(axis = 0)
Xtest_mean = Xtest.mean(axis = 0)
print("data preprocessing")
Xtrain = Xtrain - Xtrain_mean
Xtest = Xtest - Xtest_mean
```
Now, Hot encoding will convert the target variable to a matrix of 0's and 1's.
```python
print("hyper parmeter tuning and Hot Encoding")
Ytrain_hot_encoded = np_utils.to_categorical(Ytrain, num_classes = 10)
X_train, X_test, Y_train, Y_test = train_test_split(Xtrain, Ytrain_hot_encoded, train_size=0.95)
print("Model building")
print("train data shape {!s}".format(Xtrain.shape))
```
Let's create our cnn model. Use a function if you need a dynamic model.
```python
def createModel():
	print("creating model...")
	input_shape = None
	if K.image_data_format() == 'channels_first':
		input_shape = (1, 28, 28)
	else:
		input_shape = (28, 28, 1)
	input_img = Input(shape=input_shape)
	conv2D_1a_3x3_1 = Conv2D(64, (3, 3), strides=1, padding="same", activation="relu")(input_img)
	conv2D_1b_3x3_1 = Conv2D(64, (3, 3), strides=1, padding="same", activation="relu")(conv2D_1a_3x3_1)
	maxpool_1_3x3_1 = MaxPooling2D(pool_size=(2, 2))(conv2D_1b_3x3_1)
	conv2D_2a_3x3_1 = Conv2D(100, (3, 3), strides=1, padding="same", activation="relu")(maxpool_1_3x3_1)
	conv2D_2b_3x3_1 = Conv2D(100, (3, 3), strides=1, padding="same", activation="relu")(conv2D_2a_3x3_1)
	maxpool_2_3x3_1 = MaxPooling2D(pool_size=(2, 2))(conv2D_2b_3x3_1)
	conv2D_3a_3x3_1 = Conv2D(128, (3, 3), strides=1, padding="same", activation="relu")(maxpool_2_3x3_1)
	conv2D_3b_3x3_1 = Conv2D(128, (3, 3), strides=1, padding="same", activation="relu")(conv2D_3a_3x3_1)
	maxpool_3_3x3_1 = MaxPooling2D(pool_size=(2, 2))(conv2D_3b_3x3_1)
	final = Flatten()(maxpool_3_3x3_1)
	final = Dense(512, activation="relu")(final)
	final = Dropout(0.2)(final) 
	final = Dense(128, activation='relu')(final)
	final = Dense(10, activation="softmax")(final)
	model = Model(inputs=input_img, outputs = final)
	sgd = SGD(lr=0.1, decay=1e-6, momentum=0.9, nesterov=True)
	model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy', 'categorical_accuracy'])
	print("printing Model Summary...\n{!s}".format(model.summary()))
	return model
```

##  Training the model
Let's train the model. 

Use fit method and pass the data set and other required parameters.

```python
model = createModel()
epochs = 10
print("Model Compilation")
print("training...")
model.fit(X_train, Y_train, validation_data = (X_test, Y_test), epochs=epochs, batch_size=32, shuffle=True)
```
to save the weights use model's `save` attribute. For keras,  weights must be saved in HDF5 format.
```python
model.save('digitRecWeights.h5')
```
## Evaluting the model
this will give us three metrics defining
```python
scrs = model.evaluate(xtrain, ytrain)
print(scrs)
print("Done!")
```
## Saving the predictions
From the sample submission file we see that predictions must be in a csv file with ImageId and Label columns.

**Label** will contain the predictions. Save your predictions in a csv file.

```python
print("predicting...")
score = model.predict(Xtest, batch_size = 32)
print("Done!")
print("calculating predictions ...")
pred = np.argmax(score, axis = 1)
print("Saving predictions...")
pred = np.column_stack([np.arange(1, Xtest.shape[0]+1).reshape(-1, 1), pred])
res = pd.DataFrame(pred, columns=['ImageId', 'Label'], dtype=np.int64)
res.to_csv("final_pred.csv", index=None)
print("Done!...")
```
Phew, that was a lot, but, we finally did it!

## Output

Run your script and sit back.

This may take some time depending upon your hardware configuration.

<img src = "https://raw.githubusercontent.com/convosyn/blogs/master/blog1/blog_img_1.png" width = "500px" height = "500px"/>

<img src = "https://raw.githubusercontent.com/convosyn/blogs/master/blog1/one_out.png" width = "900px" height = "900px"/>

<img src = "https://raw.githubusercontent.com/convosyn/blogs/master/blog1/two_out.png" width = "900px" height = "900px"/>

## Submiting the Predictions
Now upload your prediction file on the kaggle site. We see that 
we are able to achieve more than 95% accuracy. Though it is not as good on a trivial dataset like digit recognition but we can achieve more accuracy by tuning our model.

Try different CNNs to see how they perform on our digit recognition dataset.
