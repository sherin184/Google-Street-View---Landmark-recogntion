# Landmark Recognition Using Google Street View Images

## Overview
This project implements a landmark recognition system using Google Street View images. A pre-trained CNN (ResNet50) with transfer learning is used to classify landmarks accurately.

## Objectives
- Load Google Street View images.
- Preprocess images.
- Train a landmark recognition model.
- Evaluate model performance.

## Dataset

```
dataset/
├── train/
├── validation/
└── test/
```

Each folder contains subfolders for different landmark classes.

## Image Preprocessing
- Resize images to **224×224**
- Convert to RGB
- Normalize pixel values (0–1)
- Apply data augmentation:
  - Rotation
  - Horizontal Flip
  - Zoom
  - Brightness Adjustment

## Model Architecture
- **Base Model:** ResNet50 (ImageNet weights)
- Global Average Pooling
- Dense (256, ReLU)
- Dropout (0.5)
- Softmax Output Layer

## Training Configuration

| Parameter | Value |
|-----------|-------|
| Image Size | 224×224 |
| Batch Size | 32 |
| Epochs | 20–30 |
| Optimizer | Adam |
| Loss | Categorical Crossentropy |

Early stopping is used to prevent overfitting.

## Workflow

```
Street View Images
        ↓
Image Preprocessing
        ↓
Data Augmentation
        ↓
ResNet50 Model
        ↓
Feature Extraction
        ↓
Landmark Classification
        ↓
Model Evaluation
```

## Evaluation Metrics
- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

## Technologies
- Python
- TensorFlow
- Keras
- OpenCV
- NumPy
- Scikit-learn
- Matplotlib

## Future Enhancements
- Real-time landmark recognition
- Google Maps integration
- Larger landmark dataset
- Web/Mobile deployment

## Conclusion
This project demonstrates landmark recognition using Google Street View images and transfer learning. The model provides accurate landmark classification and can be extended for navigation, tourism, and smart city applications.
