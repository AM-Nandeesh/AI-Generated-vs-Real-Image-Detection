# AI-Generated-vs-Real-Image-Detection

For Data set and Code : https://www.kaggle.com/code/amnandeesh/notebookb0d7290cbe

Data Preprocessing:
The code reads and preprocesses the image data, resizing the images to a specific size (96x96x3) using OpenCV.
The images are converted to arrays and normalized by dividing by 255.
Labels are assigned based on the folder names (REAL or FAKE), and one-hot encoding is applied to the labels.

Model Building:
The code defines a CNN model using the Keras Sequential API.
The model consists of multiple convolutional layers, activation functions, batch normalization, max pooling, and dropout layers.
It concludes with fully connected layers and a softmax activation for binary classification.

Model Training:
The model is compiled with an optimizer (adam) and a loss function (categorical cross-entropy).
The model.fit() function is used to train the model on the training data, with validation data provided for monitoring performance.
The training process runs for a specified number of epochs, and the loss and accuracy are displayed during training.

Evaluation:
After training, the model is evaluated on the test data.
Predictions are made using model.predict() and converted into class labels.
The true labels are also obtained by converting one-hot encoded test labels.
A classification report is generated using sklearn.metrics.classification_report to evaluate the model's performance.

Additional Testing:
The code then proceeds to test the model on a separate set of test images.
Similar to the previous evaluation, predictions are made, and a classification report is generated to assess the model's performance on the new data.
