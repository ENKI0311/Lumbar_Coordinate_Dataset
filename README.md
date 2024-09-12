# Lumbar_Coordinate_Dataset
Repository for lumbar spine coordinate prediction using CNNs on medical imaging data. Includes preprocessing, model architectures, training, and evaluation pipelines for x, y coordinate regression. Utilizes data augmentation, dropout, and batch normalization to enhance model performance and accuracy

---

# Lumbar Spine Coordinate Prediction Using CNNs

This repository contains the implementation of a convolutional neural network (CNN) model for predicting lumbar spine coordinates (x, y) from medical imaging data. The dataset consists of various medical scans, with each image corresponding to specific coordinate labels.

## Dataset Overview

The dataset comprises medical images from different angles (sagittal, coronal, axial) and includes corresponding x and y coordinates for lumbar spine points. The dataset is used for a regression task where the goal is to predict these coordinates from the images.

### Data Structure

- **Images**: Medical scans of lumbar spine regions.
- **Coordinates**: Corresponding (x, y) points indicating key locations on the spine.

The dataset is divided into training, validation, and test sets. Data augmentation and normalization techniques are applied to enhance model performance.

## Model Architecture

The CNN model is designed to process grayscale images (256x256) and predict (x, y) coordinates. The architecture includes:

- **Convolutional Layers**: Extract spatial features from the input images.
- **MaxPooling Layers**: Downsample the feature maps for computational efficiency.
- **Batch Normalization**: Normalize the activations to stabilize learning.
- **Fully Connected Layers**: Dense layers to learn from the extracted features.
- **Dropout**: Applied to prevent overfitting.

### Model Summary

- Input: 256x256 grayscale images
- Output: (x, y) coordinate predictions
- Loss Function: Mean Squared Error (MSE)
- Optimizer: Adam

## Installation

To use this repository, clone the repo and install the required packages:

```bash
git clone <repository_url>
cd <repository_directory>
pip install -r requirements.txt
```

Ensure that the dataset is properly structured and paths are correctly set in the code.

## Training

To train the model, execute the following command:

```bash
python train.py
```

This will train the CNN model on the training dataset and validate it on the validation dataset. Model checkpoints are saved during training.

### Training Parameters

- **Epochs**: 50
- **Batch Size**: 32
- **Learning Rate**: 0.001 (adjustable)

## Evaluation

To evaluate the model on the test dataset:

```bash
python evaluate.py
```

This will calculate the loss and Mean Absolute Error (MAE) on the test dataset.

## Results

The model achieves an MAE of approximately 0.49 on the validation set. Further tuning and layer adjustments are possible to improve the performance.

## Future Work

- **Fine-tuning the Model**: Experiment with deeper architectures or alternative activation functions.
- **Data Augmentation**: Further explore augmentations to improve generalization.
- **Transfer Learning**: Utilize pre-trained models to enhance performance.

## Contributing

Feel free to submit pull requests or open issues for any bugs or suggestions.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

---
