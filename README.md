# Traffic

This project implements a convolutional neural network (CNN) using TensorFlow and Keras to classify traffic signs. It is designed to work with a dataset consisting of images of traffic signs categorized into 43 different classes. The dataset should be organized in a directory where each category has its own subdirectory named after the category's numerical label.

## Dependencies

- Python 3
- TensorFlow
- Keras
- OpenCV
- NumPy
- scikit-learn

Ensure you have the required dependencies installed by running:

```
pip install tensorflow keras opencv-python numpy scikit-learn
```

## Dataset Structure

The expected dataset directory structure is as follows:

```
data_directory/
0/ # Images for category 0
1/ # Images for category 1
...
42/ # Images for category 42
```

Each subdirectory should contain images corresponding to a traffic sign category, with the subdirectory's name being the category's numerical label.

## Usage

To use this script, you should have your dataset prepared according to the specified structure. Run the script by passing the path to the dataset directory as the first command-line argument. Optionally, you can specify a second argument to save the trained model to a file:

```
python traffic.py data_directory [model.h5]
```

## Features

- **Data Loading and Preprocessing**: Automatically loads and resizes images from the dataset directory. The script expects the data to be organized in subdirectories corresponding to each category.
- **Model Architecture**: Implements a CNN with the following layers:
  - Two convolutional layers with ReLU activation and max pooling.
  - A flattening layer to convert the 2D feature maps to a 1D vector.
  - A dense layer with ReLU activation and dropout for regularization.
  - An output dense layer with softmax activation to classify the 43 different traffic sign categories.
- **Training and Evaluation**: Splits the dataset into training and testing sets, trains the CNN on the training set, and evaluates its performance on the testing set.
- **Model Saving**: Optionally saves the trained model to a file for later use.