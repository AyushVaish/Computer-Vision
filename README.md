# Cat vs. Dog Classifier (Computer Vision)

## Abstract
This project builds a binary image classifier to distinguish between cats and dogs using convolutional neural networks (CNNs). We explore both a custom CNN trained from scratch and transfer‐learning approaches (e.g., VGG16, ResNet50) to maximize accuracy while keeping training time reasonable.

## Problem Statement
Automated image classification of pets (cats vs. dogs) is a classic computer vision task with applications in photo organization, pet‐care apps, and social media filtering. The goal is to train a model that, given an input image, predicts whether it contains a cat or a dog with high accuracy.

- **Image Size**: Varies; will be resized to 150×150 or 224×224 pixels

## Data Preprocessing
1. **Image resizing** to a uniform resolution (e.g., 150×150 for a custom CNN, 224×224 for transfer models)  
2. **Normalization**: pixel values scaled to [0, 1]  
3. **Data augmentation** (applied to training set only):  
   - Random flips (horizontal/vertical)  
   - Random rotations  
   - Random zooms and shifts  

## Model Architectures
- **Custom CNN**  
  - 3 convolutional blocks (Conv → ReLU → Pool)  
  - 2 fully connected layers + Dropout  
- **Transfer Learning**  
  - **VGG16 (pretrained on ImageNet)**  
  - **ResNet50 (pretrained on ImageNet)**  
  - Freeze base layers, train custom classifier head; then optionally fine‑tune top layers

