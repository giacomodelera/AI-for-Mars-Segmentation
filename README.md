# AI-for-Mars-Segmentation

## Abstract
Terrain type detection and image segmentation are two crucial tasks involved in modern Martian missions to ensure rovers correctly follow an appropriate path and interact with the environment according to missions and experiments.

This project focuses on image segmentation of martian soil pictures, aiming to develop a deep learning model for segmenting images of Mars terrain into five distinct classes: background, soil, bedrock, sand, and big rocks.

The dataset available is composed of grey-scale images, paired with masks with pixel-wise class-segmentation. Due to class imbalance and camera perspective, several operations have to be performed on it from the get-go, in order to obtain a good level of accuracy.
The architecture of choice is the U-Net architecture. The robust ability of this architecture to contract the image, extract context, and expand the image to localise the image has proven effective in various segmentation tasks.

Due to the specific context our U-Net implementation is trained on (Martian soil segmentation), an appropriate choice of the loss function has to be taken into consideration in order to learn both global and local features of the given terrain images and associated pixel-wise classes.

## Context
This project is an AI-based solution developed for Mars segmentation as part of a competition. The goal was to accurately detect and distinguish different zones of Mars terrain from images. 
The project utilizes deep learning models and image processing to achieve high segmentation accuracy. 

## Repository Structure
* [Report](Report.pdf)
  contains a deeper description of the problem and a detailed explanation of the methodologies.
* **`Code/`**
  
  **`1_dataset_augmentation`** contains code for augmenting the dataset by applying various transformations (e.g., rotation, flipping, scaling) to the images.
  
  **`2_model_training`** is responsible for training the AI model. It loads the augmented dataset, sets up the deep learning architecture, and trains the model using the appropriate loss function and optimization     technique.

