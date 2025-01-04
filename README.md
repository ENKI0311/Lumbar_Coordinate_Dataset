

---

# Lumbar Spine Coordinate Prediction Using CNNs

## Overview
This repository implements a **Convolutional Neural Network (CNN)** for predicting **lumbar spine coordinates (x, y)** from medical imaging data. It includes data preprocessing, model design, training pipelines, and evaluation scripts for regression tasks. Key techniques such as data augmentation, dropout, and batch normalization are employed to enhance model accuracy and robustness.

---

## Dataset Overview

The dataset contains medical images of the lumbar spine along with their corresponding (x, y) coordinate labels. These labels indicate specific anatomical points on the spine.

### **Data Structure**
- **Images**: Medical scans of lumbar spine regions (e.g., sagittal, coronal, axial views).
- **Coordinates**: Corresponding (x, y) points for key spinal locations.

The dataset is split into:
- **Training Set**
- **Validation Set**
- **Test Set**

**Data Augmentation** and **Normalization** are applied to improve model performance.

---

## Model Architecture

The CNN processes grayscale images (256x256 resolution) to predict two continuous values: **x** and **y** coordinates. Key components include:

- **Convolutional Layers**: Extract spatial patterns from images.
- **MaxPooling Layers**: Downsample feature maps to reduce computational cost.
- **Batch Normalization**: Stabilize and accelerate learning by normalizing activations.
- **Dropout Layers**: Mitigate overfitting by randomly deactivating neurons during training.
- **Fully Connected Layers**: Map extracted features to coordinate predictions.

### **Model Summary**
- **Input**: 256x256 grayscale images
- **Output**: Predicted (x, y) coordinates
- **Loss Function**: Mean Squared Error (MSE)
- **Optimizer**: Adam

---

## Installation

To set up the project locally:

1. Clone the repository:
   ```bash
   git clone <repository_url>
   cd <repository_directory>
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

Ensure the dataset is correctly structured, and file paths are set in the code.

---

## Usage

### **Training**
To train the model:
```bash
python train.py
```
- **Default Training Parameters**:
  - Epochs: 50
  - Batch Size: 32
  - Learning Rate: 0.001

The script saves model checkpoints during training for later evaluation or fine-tuning.

### **Evaluation**
To evaluate the model on the test dataset:
```bash
python evaluate.py
```
This computes performance metrics such as **Mean Absolute Error (MAE)** and **Loss** on the test set.

---

## Results

- **Validation MAE**: ~0.49
- **Test Performance**: Results may vary based on hyperparameter tuning and data augmentation.

### **Sample Visualizations**
Visualization scripts are included to plot:
- Predicted vs. True coordinates
- Loss curves during training

---

## Future Work

1. **Model Fine-Tuning**: Experiment with deeper CNN architectures or alternative activation functions.
2. **Enhanced Augmentation**: Explore advanced augmentation techniques to improve model generalization.
3. **Transfer Learning**: Leverage pre-trained models for enhanced feature extraction.
4. **3D Imaging Support**: Extend the model to process 3D scans for comprehensive spinal analysis.

---

## Project Structure

```
Lumbar_Coordinate_Dataset/
├── data/                   # Dataset and related files
├── models/                 # Saved models and checkpoints
├── scripts/                # Training, evaluation, and utility scripts
├── results/                # Evaluation results and visualizations
├── requirements.txt        # Python dependencies
├── README.md               # Project documentation
└── LICENSE                 # License information
```

---

## Contributing

Contributions are welcome! If you want to enhance the project:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add feature-name"`).
4. Push to the branch (`git push origin feature-name`).
5. Open a pull request for review.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

