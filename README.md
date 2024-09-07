# IR_Pedestrian_Project

This Python code is an example of a deep learning project that uses a Convolutional Neural Network (CNN) for pedestrian detection. The code performs the following main steps:

- Importing Required Libraries
torch, torch.nn, torch.nn.functional: PyTorch libraries used for model creation, training, and testing.
PIL: Used for processing images.
matplotlib, numpy, os, time: Used for data visualization, data processing, and timing calculations.

- Device Configuration
torch.device: Utilizes GPU if available; otherwise, it defaults to CPU. This impacts the speed of computations.

- Loading and Processing Images
read_images(): Reads images from a specified directory, converts each image to a one-dimensional array, and stores it in a NumPy array.

- Loading Training and Test Data
Training and test data are loaded from both negative and positive classes (pedestrian and non-pedestrian).
Images from both classes are converted to tensors and prepared with labels.

- Visualizing Images
An image from the training data is visualized in grayscale.

- Creating the CNN Model
The Net class defines a CNN model with two convolutional layers and three fully connected layers.
Model structure: two convolutional layers, two pooling layers, and three fully connected layers.

- Preparing the Model for Training and Testing
Training and test datasets are prepared using PyTorch DataLoader.
The model is trained with CrossEntropyLoss as the loss function and SGD for optimization.

- Training and Testing the Model
During training: The model’s weights are updated each epoch, and training accuracy is calculated.
During testing: The model’s accuracy is evaluated on the test dataset.
Training and test results are monitored and visualized over time.

- Visualizing Results
Training and test accuracies, along with loss values, are visualized.
