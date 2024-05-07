#                           Fraud News Detection

## Aim : 
    This Project aims to predict whether the given news by the user is fake or not.

    
## Algorithm Used : 
    1. Neural Networks , 
    2. Natural Language Processing , 
    3. Long Short Term Memory(LSTM).


## Steps :
### Importing Libraries and Dataset :
    This section imports necessary libraries, particularly pandas for data manipulation and reading CSV files. It reads a CSV file named 'train.csv' into a DataFrame called df and displays the first few rows of the DataFrame.

### Data Preprocessing :
    Any rows containing missing values (NaN) are dropped from the DataFrame. Then, the input features (X) are separated from the target variable (y).

### Text Preprocessing :
    Text preprocessing tasks such as removing non-alphabetic characters, converting text to lowercase, tokenization, removing stopwords, and stemming using NLTK library takes place at this section.

### Text Encoding : 
    The text data is encoded using one-hot encoding, converting words into numeric vectors of fixed size.

### Padding Sequences :
    The encoded sequences are padded to ensure uniform length using the pad_sequences function from Keras.

### Model Building :
    A Sequential model is created using Keras. It consists of an Embedding layer, an LSTM layer, and a Dense layer. The model is compiled with binary cross-entropy loss and Adam optimizer.

### Model Training : 
    The model is trained on the training data (X_train and y_train) for 10 epochs with a batch size of 64.

### Model Evaluation :
    The model's performance is evaluated on the test data (X_test and y_test) using the evaluate method.

### Saving the Model :
    The trained model is saved using both pickle and the HDF5 format.

### Making Predictions :
    Finally, the trained model is used to make predictions on new data, in this case, a single input sentence (word_to_predict). The output prediction is then used to determine if the news is real or fake based on a threshold value.

## Result :
    This code essentially demonstrates the process of building a deep learning model using Keras for text classification (real vs. fake news) and saving the model for future use.
