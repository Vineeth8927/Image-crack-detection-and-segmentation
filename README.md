# Image-crack-detection-and-segmentation
# Crack Segmentation using Deep Learning

This repository contains code for segmenting cracks in images using deep learning, specifically employing a U-Net architecture and, optionally, a Feature Pyramid Hierarchical Boosting Network (FPHBN). This project can be used for various applications, such as infrastructure inspection, quality control, and material analysis.

## Dataset

The code is designed to work with datasets containing images and corresponding binary masks, where the masks highlight the crack regions. The dataset used in the original Colab notebook was the Crack500 dataset. You can adapt the code to use your own dataset by modifying the data paths.

## Models

This repository includes implementations of the following models:

*   **U-Net:** A widely used convolutional neural network architecture for image segmentation. It consists of an encoder path to capture context and a decoder path to enable precise localization.
*   **Feature Pyramid Hierarchical Boosting Network (FPHBN):** A more advanced architecture that uses a feature pyramid and hierarchical supervision to improve segmentation performance. (This is in the updated code but was not in the initial version).

## Key Features

*   **Data Augmentation:** Implements data augmentation techniques (rotations, shifts, flips, zooms) to improve model robustness and generalization.
*   **Multi-GPU Training:** Supports multi-GPU training using TensorFlow's `MirroredStrategy`.
*   **Training and Validation Monitoring:** Includes callbacks for model checkpointing, early stopping, and learning rate reduction on plateau.
*   **Comprehensive Evaluation:** Evaluates the model using loss, accuracy, and Mean Intersection over Union (IoU) metrics.
*   **Visualization:** Provides functions for visualizing training history, predictions, and prediction overlays on original images.
*   **TensorBoard Integration:** Includes TensorBoard callbacks for visualizing training progress.

## Requirements

*   Python 3.7+
*   TensorFlow 2.x
*   OpenCV (cv2)
*   NumPy
*   Matplotlib
*   (Optional) Kaggle API (if using the Crack500 dataset directly from Kaggle)

You can install the required packages using pip:

```bash
pip install tensorflow opencv-python numpy matplotlib
