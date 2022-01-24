#convolutional-neural-nets

%------------------------------------ Data Set --------------------------------------%

The MNIST handwriting database comes pre-loaded with a set of 60,000 training images and 10,000 testing images. Each image in MNIST has 28 x 28 pixels, and represents a handwritten number between 0 and 9. 

We split the pre-set training images into 48,000 training images and 12,000 validation images. 



%------------------------------------ Goal of the Project --------------------------------------%

Create a convolutional neural network using Keras. 

##### Model 1 

The layout of the Convolutional Neural Net is as follows:

	1. Take a 28x28 pixel image from MNIST

	2. Apply 32, 5x5 filters **without** the same padding 

	3. Maxpool with 2x2 frames

	4. Apply 64, 5x5 filters **without** the same padding

	5. Maxpool with 2x2 frames

	6. Pass into a fully connected layer with 128 neurons and relu activation

	7. Dropout (a percentage of randomly selected neurons ignored during training)

	8. Pass into a layer with 10 neurons and softmax activation (these will be our outputs, the highest value will tell us which class to place the image in)

Only saves the model for the best validation loss. 

We report the training, validation, and out of sample testing accuracy. 


##### Model 2 

The layout of the Convolutional Neural Net is as follows:

	1. Take a 28x28 pixel image from MNIST

	2. Apply 32, 3x3 filters **with** the same padding

	3. Maxpool with 2x2 frames

	4. Apply 32, 3x3 filters **with** the same padding

	5. Maxpool with 2x2 frames

	6. Pass into a fully connected layer with 128 neurons and relu activation

	7. Dropout (a percentage of randomly selected neurons ignored during training)

	8. Pass into a layer with 10 neurons and softmax activation (these will be our outputs, the highest value will tell us which class to place the image in)


We report the training, validation, and out of sample testing accuracy. 

%------------------------------------ Required Packages --------------------------------------%

	keras

	datetime

	numpy

	(optional) tensorboard (will require running the following command in terminal: pip install jupyter-tensorboard)