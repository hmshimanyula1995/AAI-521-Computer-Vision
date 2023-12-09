# AAI-521-Computer-Vision

# Full Body Segmentation Project

This repository contains the code for training a U-Net model on the MADS dataset for the purpose of full-body segmentation.

## Overview

The project uses a U-Net model architecture to perform image segmentation to identify the human figure within images. It includes preprocessing of images and masks, training with early stopping, loss and accuracy visualization, and saving the trained model.

## Code Structure

- Mounting Google Drive (if using Colab) to access the dataset.
- Setting up paths for images, masks, and collages.
- Loading and preprocessing of the dataset including images and masks.
- Definition of a custom `Dataset` class to handle the image transformation and loading.
- Creation of training and validation DataLoaders.
- Training function definition to perform the forward and backward propagation.
- Evaluation function definition for model validation.
- Model training loop that saves losses and accuracies per epoch.
- Visualization of training and validation losses and accuracy using matplotlib.
- Saving the trained model as a `.pth` file for future use.

## Instructions

1. Ensure the dataset is placed in the correct directories or update the paths accordingly.
2. Run the training script to start the training process.
3. Visualize the results with the provided plotting code.
4. The final model can be saved and loaded for future inference.

## Model Training

The model is trained using cross-entropy loss with an AdamW optimizer. Early stopping is applied based on validation loss to prevent overfitting.

## Visualization

Loss and accuracy graphs are plotted to show the model's performance over epochs, aiding in the evaluation of the training process.

## Saving the Model

After training, the model's state dictionary is saved to `model.pth`, allowing it to be loaded and used for predictions later.
