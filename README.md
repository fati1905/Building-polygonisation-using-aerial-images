# Building Polygonization from Satellite Images

## Overview

This project aims to extract building footprints from satellite images using **Deep Learning** techniques. Specifically, it uses a **neural network** architecture to predict the **vertices** of buildings and subsequently **polygonize** the building boundaries. The model leverages the power of pre-trained networks such as **ResNet-34** for feature extraction, combined with post-processing techniques like **Convex Hull** to refine the predictions into accurate polygons.

## Project Structure

The project consists of multiple key components:

1. **Data Preprocessing**: 
   - Loading, resizing, and splitting of the satellite images and their corresponding ground truth masks.
   - Conversion of the masks into a format suitable for training, e.g., extracting contours as vertices.

2. **Model Architecture**: 
   - A **U-Net** inspired architecture with a pre-trained **ResNet-34** backbone.
   - The model outputs predicted **vertices** of buildings, which are then used to construct polygons (building footprints).

3. **Post-processing**: 
   - The predicted vertices are used to form **Convex Hulls** which generate closed polygons outlining the building footprints.

4. **Visualization**: 
   - The predicted polygons and their corresponding vertices are visualized over the original satellite image.
![image](https://github.com/user-attachments/assets/157c77d6-6ce5-4913-8e12-f5d01fd7de54)

---

## Installation

To run this project, you will need the following dependencies:

1. **This is a notebook, can be directly run in Google Colab or similar tool**
2. **Mind the changes of paths and dataset availability** 

## Results
A few results of this project : 

![image](https://github.com/user-attachments/assets/818018d8-6797-450f-a81b-99a4309902e1)
![image](https://github.com/user-attachments/assets/eee983cd-fa86-469a-8f07-e2dc94fb6f11)

**More examples can be directly reviewed in the notebook.**
Please mind, that some results are not perfect espicially that the segmentation Map was not deployed in the model architecture. 

