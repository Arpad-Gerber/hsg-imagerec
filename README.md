# **Group project: Machine Learning with Python (digit recognition)**

**Group members** <br/>
Arpad Gerber <br/>
Dominik Lanter<br/>
Justus Hofmann


**About** <br/>
This is a student project of the university of St. Gallen of the course Programming with Advanced Computer Languages. <br/>
The goal of the project was to create a supervised  machine learning classifier which recognises hand written digits from 0 to 9.
The classifier is based on training and test data sets provided by the MNIST data base. We enhanced the program by adding a feature that allows the user to feed the classifier with images of self-written digits. These images can be in PNG or JPEG format. The program output is the final digit classification.


**Pre-requisites** <br/>
The program is coded in Python3. The following libraries need to be installed prior to running the program: <br/>
*numpy, tensorflow, keras, sklearn, PIL, matplotlib*

**Instructions** <br/>
1. Prior to starting the programm, you might want to add some additional self-written images of digits to the folder
2. Run the file Project_version_3.ipynb
3. Choose which digit you want to classify by changing the file name of the respective image in the image converter
4. The output should give the digit classification as well as a plot showing the recognition probabilites

**Description** <br/>
First, we prepare the data. We load data sets for training and testing from the mnist package. We found this package more convenient than downloading and importing the data ourselves. We then bring the data sets into a form that is optimized for the learning model and normalize values to the range from 0 to 1. <br/>
Second, we build a sequential model based on a convolutional neural network using *tensorflow* and *keras*. We then optimize and finally compile it. <br/>
Thirdly, we fit the established model using the training data sets. We evaluate the model by looking at the test accuracy and find that the out-of-sample precision of 98.7% is sufficiently accurate. <br/>
Next, we import an image file of our handwritten digits. The image is then resized to 28x28 pixels, centered, and the colors are inverted as the training data are images of white digits on black ground. After that, we convert the image into the format that our classifier model is based on. <br/>
Finally, we let the model predict the digit of the input image. As an output, we provide the recognised digit and an additional chart with the different probabilities of the prediction.

**Sources** <br/>
data sets: http://yann.lecun.com/exdb/mnist/tutorial <br/>
*tensorflow* tutorial: https://machinelearningmastery.com/how-to-develop-a-convolutional-neural-network-from-scratch-for-mnist-handwritten-digit-classification/#:~:text=MNIST%20Handwritten%20Digit%20Classification%20Dataset,-The%20MNIST%20dataset&text=It%20is%20a%20dataset%20of,from%200%20to%209%2C%20inclusively <br/>
*keras* tutorial: https://www.datacamp.com/community/tutorials/deep-learning-python <br/>
