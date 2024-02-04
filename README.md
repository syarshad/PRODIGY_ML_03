This project focuses on building a machine learning model to classify images of dogs and cats using Support Vector Machines (SVM). The dataset used contains a collection of images of dogs and cats.

# Methods Used:

## Data Preparation:
The dataset was obtained as a zip file and extracted using the zipfile library.
Images were resized to a standard size (128x64 pixels) using the resize function from the skimage.transform module.
Histogram of Oriented Gradients (HOG) feature extraction technique was applied to convert the images into a feature vector representation suitable for training the model.

## Feature Extraction:
HOG feature descriptors were computed for each image using the hog function from the skimage.feature module.
HOG features capture the shape and texture information of the images, which are crucial for image classification tasks.

## Model Training:
Two SVM models were trained using different SVM implementations:

## LinearSVC Model: 
A linear Support Vector Classifier (LinearSVC) was trained using the LinearSVC class from the sklearn.svm module.
SVC Model with Linear Kernel: Another SVM model with a linear kernel was trained using the SVC class from the sklearn.svm module, specifying the kernel as 'linear'.
The models were trained on the extracted HOG features (X) and corresponding labels (Y) indicating whether the image depicts a dog (1) or a cat (0).

## Model Evaluation:
The accuracy of each model was evaluated using the score method on the test data (X_test, y_test) obtained through train-test split.

# Results:
The LinearSVC model achieved an accuracy of approximately 67.33% on the test data.
The SVM model with a linear kernel achieved a slightly higher accuracy of approximately 68%.
