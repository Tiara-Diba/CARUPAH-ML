# CARUPAH-ML
This is a repository for C23-PS062 Machine Learning

## CARUPAH
Carupah is an application that allows users to detect types of waste, interact with chatbots, and get information about the nearest waste bank. There are two machine-learning implementations in this application image detection and chatbot. Image detection helps users classify the type and type of waste, while the chatbot feature functions as knowledge management.

### Image Detection
#### 1. Setup the Data
   
#### 3. Data Preprocessing
#### 4. Build a Model
#### 5. Save Model



### Chatbot
Chatbot in Carupah Application named CarupAI. It is built with Natural Language Processing with the TensorFlow framework. We created our own dataset in JSON format and saved it to Google Drive. To replicate our code just simply download it and run it in Google Colab. The work of this code is divided into all steps below:
#### 1. Setup the Data
Get datasets stored in Google Drive using the request library and decodes byte content into a string.
#### 3. Data Preprocessing
Using Natural Language Tool Kit library 
- Tokenization: Dividing text into smaller units called tokens in the form of words, phrases, or symbols using punkt package.
- Lemmatization: Converting words to their basic form called a root word using wordnet package.
#### 4. Build a Model
We use the Keras library to build and train the Natural Language Processing neural network model with TensorFlow as the backend.
- Sequential Model: Builds the model sequentially, where each layer is added one by one in order
- Dense Layer: Adding representation capacity to the model
- Dropout Layer: Prevent overfitting
- Activation Layer: Introduces non-linearities that are necessary for modeling complex data
- SGD (Stochastic Gradient Descent) as a optimizer
#### 5. Train Model
The fit() method is used to initialize the training of the model with the given training data.
#### 5. Save Model
Save the trained model into a file with HDF5 format. 
#### 6. Load Sources
- Load dataset
- Load a previously saved object in a pickle file
- Load model HDF5
#### 7. Testing Preparation
Create function for:
- Cleaning input sentences (Tokenization & Lemmatization)
- Converts the input sentence into a bag of words vector representation
- Prediction of classes or intents based on input sentences using trained models
- Get the appropriate response based on the intent predicted by the model
#### 8. Testing
Create a function for chatbot flow to interact with the chatbot and get answers to questions based on user intent.
