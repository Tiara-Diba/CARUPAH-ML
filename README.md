# CARUPAH-ML
This is a repository for C23-PS062 Machine Learning

## CARUPAH
Carupah is an application that allows users to detect types of waste, interact with chatbots, and get information about the nearest waste bank. There are two machine-learning implementations in this application image detection and chatbot. Image detection helps users classify the type and type of waste, while the chatbot feature functions as knowledge management.

### Image Detection
We build image detection with classification method. The resulting classification is a classification of waste based on the type of waste. This feature is formed using Convolutional Neural Network with Tensorflow framework. We use a dataset containing photos of various types of waste and store it in the local environment. To replicate our code just simply download it and run it in the Code Editor, Anaconda, or Python IDE  that are available in the local environment. The work of this code is divided into all steps below:
#### 1. Setup the Data
First install and import all required package to run the codes. After that locate the dataset in Google Drive or in the local environment. Install the Split-folders Python package to split the dataset into training and validation datasets.
#### 3. Data Preprocessing
First, define variables to store the desired height and width data of the image. After that, perform data augmentation using the tf.keras.preprocessing.image module in TensorFlow. Here are the tools used in preprocessing:
  - ImageDataGenerator = This class is used to perform real-time image data augmentation while training the model. ImageDataGenerator performs data transformations such as rotating, widening, normalizing or rescaling the pixel values in the image, and so on. This class serves to prevent overfitting.
  - flow_from_directory = Methods provided by the ImageDataGenearator class. This method is used to load the data to be used, generate a batch of images, the desired image size, and set the class label return mode of the data generator. We value the 'class_mode' parameter to be sparse, since the dataset has more than 1 class
  - After performing the augmentation function, proceed with loading the training and validation datasets into the Data Augmentation function.
#### 4. Build a Model
We use the Keras library to build and train the Convolutional Neural Network model with TensorFlow as the backend.
- Sequential Model: Builds the model sequentially, where each layer is added one by one in order
- Conv2D layer: The fundamental to build block of a CNN. It perfomrs convolutional operations on input data (mainly for images).
- MaxPooling2D layer: This layer is used to downsamples the spatial dimensions of the input feature maps while retaining the most important information.
- Flatten layer: This layer is used to convert the multi-dimensional output from the preciding convolutional or pooling layers into a one-dimensional vector.
- Dense Layer: Adding representation capacity to the model
- Dropout Layer: Prevent overfitting
- Activation Layer: Introduces non-linearities that are necessary for modeling complex data
- RMSprop (Root Mean Square Propagation) as a optimizer
#### 5. Train and validate model
First create the model with the 'create_model()' method. After that use the fit() method to initialize the training and validation of the model with the given training and validation data.
#### 6. Analyze the result of the model
Here we can use matplotlib.pyplot to visualize the training and validation of our model. These include the loss in training and validation, and the accuracy in training and validation on each epoch.
#### 7. Save Model
Lastly save the trained model into a file with HDF5 format and tflite.


### Chatbot
Chatbot in Carupah Application named CarupAI. It is built with Natural Language Processing with the TensorFlow framework. We created our own dataset in JSON format and saved it to Google Drive. To replicate our code just simply download it and run it in Google Colab. The work of this code is divided into all steps below:
#### 1. Setup the Data
Get datasets stored in Google Drive using the request library and decodes byte content into a string.
#### 2. Data Preprocessing
Using Natural Language Tool Kit library 
- Tokenization: Dividing text into smaller units called tokens in the form of words, phrases, or symbols using punkt package.
- Lemmatization: Converting words to their basic form called a root word using wordnet package.
#### 3. Build a Model
We use the Keras library to build and train the Natural Language Processing neural network model with TensorFlow as the backend.
- Sequential Model: Builds the model sequentially, where each layer is added one by one in order
- Dense Layer: Adding representation capacity to the model
- Dropout Layer: Prevent overfitting
- Activation Layer: Introduces non-linearities that are necessary for modeling complex data
- SGD (Stochastic Gradient Descent) as an optimizer
#### 4. Train Model
The fit() method is used to initialize the training of the model with the given training data.
#### 5. Visualize Loss and Accuracy
Visualize the change in loss and accuracy at each epoch of model training to analyze model performance, identify overfitting or underfitting, and monitor training progress.
#### 6. Save Model
Save the trained model into a file in HDF5 format. 
#### 7. Load Sources
- Load dataset
- Load a previously saved object in a pickle file
- Load model HDF5
#### 8. Testing Preparation
Create function for:
- Cleaning input sentences (Tokenization & Lemmatization)
- Converts the input sentence into a bag of words vector representation
- Prediction of classes or intents based on input sentences using trained models
- Get the appropriate response based on the intent predicted by the model
#### 9. Testing
Create a function for chatbot flow to interact with the chatbot and get answers to questions based on user intent.
#### 10. Convert the model to TensorFlow.js

## Contributor
1. Irfan Kamal (Machine Learning Engineer)
2. Jonathan Henock Alexander Manik (Machine Learning Engineer)
3. Tiara Diba (Machine Learning Engineer)
4. Delliana Putri Salsabila (Cloud Computing Engineer)
5. Husna Fadillah Rahman (Cloud Computing Engineer)
6. Raihan Fadhlal Aziz (Android Engineer)
