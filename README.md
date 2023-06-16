# CARUPAH-ML
This is a repository for C23-PS062 Machine Learning

## CARUPAH
Carupah is an application that allows users to detect types of waste, interact with chatbots, and get information about the nearest waste bank. There are two machine-learning implementations in this application image detection and chatbot. Image detection helps users classify the type and type of waste, while the chatbot feature functions as knowledge management.
*
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
- Tokenization: Dividing text into smaller units called tokens in the form of words, phrases, or symbols.
- Lemmatization: Converting words to their basic form called a root word.
#### 4. Build a Model
We use the Keras library to build and train the Natural Language Processing neural network model with TensorFlow as the backend.
- Sequential: Builds the model sequentially, where each layer is added one by one in order
- Dense: Adding representation capacity to the model
- Dropout: Prevent overfitting
- Activation: Introduces non-linearities that are necessary for modeling complex data
- SGD (Stochastic Gradient Descent) as a optimizer
#### 5. Save Model
#### 6. Load Sources
#### 7. Testing Preparation
#### 8. Testing
