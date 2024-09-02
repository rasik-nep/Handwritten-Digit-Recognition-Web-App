# Handwritten Digit Recognition

This project demonstrates handwritten digit recognition using a Convolutional Neural Network (CNN) trained on the MNIST dataset. The trained model is saved and converted for use in TensorFlow.js to enable web-based predictions.

## Model Architecture

The CNN model consists of the following layers:

1. **Conv2D**: (None, 26, 26, 32) - 320 parameters
2. **MaxPooling2D**: (None, 13, 13, 32) - 0 parameters
3. **Conv2D**: (None, 11, 11, 64) - 18,496 parameters
4. **Conv2D**: (None, 9, 9, 64) - 36,928 parameters
5. **MaxPooling2D**: (None, 4, 4, 64) - 0 parameters
6. **Conv2D**: (None, 2, 2, 64) - 36,928 parameters
7. **Flatten**: (None, 256) - 0 parameters
8. **Dense**: (None, 64) - 16,448 parameters
9. **Dense**: (None, 10) - 650 parameters

**Total Parameters**: 108,770

## Training Details

- **Batch Size**: 60
- **Epochs**: 5
- **Batches per Epoch**: 1000 (calculated as `60000 / 60`)

Each epoch represents a complete run of all training samples, with a total of 5 epochs completing 5 runs of all samples.

## File Formats

- **Model Architecture**: Saved as a JSON file.
- **Model Weights**: Saved as a `.h5` file.

## Conversion to TensorFlow.js

The trained model is converted to TensorFlow.js Layers format for use in a web application.

## Accuracy

The model has an accuracy of 99.26999807357788 on the test set.
