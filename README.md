# License Plate Recognition

This project recognizes license plate numbers from images using a combination of image processing techniques and Convolutional Neural Networks (CNNs).

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Model Architecture](#model-architecture)
- [Training](#training)
- [Evaluation](#evaluation)
- [Usage](#usage)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Overview

The goal of this project is to accurately recognize license plate numbers from images. This involves several steps including license plate detection, character segmentation, and character recognition.

## Dataset

The dataset consists of images of vehicles with visible license plates. These images are annotated with the corresponding license plate numbers.

## Preprocessing
Images are first processed to detect and extract the license plate region.
Techniques used include converting images to grayscale, applying Gaussian blur, and thresholding.
The extracted license plate images are then segmented into individual characters.
This involves applying morphological operations to highlight characters and segment them.

## Model Architecture
The character recognition model consists of:

3 Conv2D layers followed by MaxPooling2D and BatchNormalization layers for feature extraction.
A Flatten layer to convert the 2D feature maps into a 1D vector.
Dense layers for classification with dropout regularization to prevent overfitting.

## Training

Optimizer: Adam with a learning rate of 0.0001.
Loss function: Sparse categorical cross-entropy for character recognition.
Metrics: Accuracy for evaluating character recognition performance.
Batch size: 32
Number of epochs: 30

## Evaluation

The model is evaluated on a separate test set of license plate images. Performance is assessed based on the accuracy of recognized license plate numbers.
## Usage

To recognize license plate numbers from new images:

Preprocess the image to extract the license plate region.
Segment the license plate image into individual characters.
Load the trained character recognition model.
Predict the characters using the model and construct the license plate number.

## Results
The model achieved ~95% accuracy after 5 times and at the end of training, it achieved ~95% accuracy on the validation set.

## Contributing

Feel free to submit issues or pull requests. Contributions are welcome!

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
