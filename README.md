# Digit-Recognizer-using-CNN
## About
The project was build inorder to recognize the digits (0-9). The application contains two csv files namely train.csv and test.csv<br>
<strong>train.csv</strong> contains 42000 rows x 785 columns. First column contains the label of the digit and the next 784 columns contains each pixel value of the digit.<br>
<strong>test.csv</strong> contains 28000 rows × 784 columns. It contains only the pixel columns of the digit for testing purpose.<br>
Each image is 28 pixels in height and 28 pixels in width.<br>
Each pixel has a single pixel-value associated with it, indicating the lightness or darkness of that pixel, with higher numbers meaning darker. This pixel-value is an integer between 0 and 255, inclusive.<br>
The dataset was obtained from [kaggle](https://www.kaggle.com/c/digit-recognizer/data)
## Layers:
1. First Convolution Layer
    * No. of filters = 32
    * Filter lengh = (3,3)
    * Activation = relu
    * input_shape = (28, 28, 1)
2. First Pooling layer
    * pool_size = (2, 2)
3. Second Convolution Layer
    * No. of filters = 32
    * Filter lengh = (3,3)
    * Activation = relu
4. Second Pooling layer
    * pool_size = (2, 2)
5. Flatten layer
6. First Fully Connected Layer
    * kernel_initializer = uniform
    * Activation = relu 
    * units=100
7. Output layer
    * kernel_initializer = uniform
    * Activation = softmax
    * units=10

<br>optimizer = adam
<br>loss = sparse_categorical_crossentropy
<br>metrics = accuracy
### Validation accuracy = 0.985
## The Repository contains the following:
- ReadMe file (current file)
- Juptyer notebook
- train.csv
- test.csv
## Requirements and Dependencies
- Python 3.7.4
- tensorflow-gpu == 1.13.0
- cufflinks == 0.17.3
- chart-studio == 1.1.0
