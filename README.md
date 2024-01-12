# Mebe: Pothole Severity Classification System

## Overview

**Mebe** is an innovative ensemble approach designed to classify the severity of potholes in streets through the integration of deep learning and image processing techniques. This README provides an in-depth understanding of the system architecture, training methodologies, and its potential applications.
![Mebe Overview](ensemble.png)
## Localization of Potholes

To effectively localize potholes, we employed a combination of state-of-the-art deep learning models, each specialized in different aspects:

1. **YOLOv8**: Localizes and classifies potholes based on severity.
2. **YOLOv5**: Enhances localization and adds classification capabilities.
3. **Faster RCNN Inception Resnet V2 1024x1024**: Focuses on precise localization.

These models were trained on distinct datasets, ensuring diversity and reducing overfitting:

- Smartathon Theme 2 road potholes dataset (Manually Annotated)
- Smartathon Theme 1 dataset (Multitask learning for better feature understanding)
- CRDDC 2022 dataset

The ensemble system fuses the outputs using weighted boxes fusion, with higher weights assigned to models trained on Theme 2 dataset.

## Estimation of Pothole Magnitude

The system includes a Dimension Estimation Module, utilizing image processing to estimate the depth and area of detected potholes. By applying the triangle similarity property, the module calculates the perceived focal length, enabling accurate determination of pothole dimensions.

## Potential Applications

### 1. Accurate Pothole Detection

Mebe demonstrates high accuracy in pothole detection by leveraging multiple models trained on diverse datasets. The ensemble approach ensures robust results, with learning curves indicating satisfactory performance.

### 2. Precise Magnitude Estimation

The system excels in estimating the magnitude of potholes, classifying them into various types and severity levels. The proposed methodology enhances accuracy by combining class weights, severity weights, and area estimation.

### 3. Identification of Urgent Potholes

Mebe establishes urgency through a ranking algorithm, considering class weights, severity weights, and estimated area. This ensures that the most problematic potholes are prioritized in the analysis.

## Lidar Comparison

While computer vision technology can enhance pothole detection, Mebe may not entirely replace Lidar due to Lidar's advantages in low-light and adverse weather conditions. However, Mebe is trained to handle diverse weather conditions and different illumination levels, providing a cost-effective alternative for many scenarios.

## Solution Autonomy and Scalability

The system minimizes human intervention, requiring only initial camera setup and calibration. Mebe's intelligent interface facilitates easy access to insights and notifications. The solution is scalable, user-friendly, and operates with minimal computational resources, making it suitable for real-time applications.

For detailed implementation instructions and requirements, please refer to the documentation provided. Feel free to reach out for any further inquiries or assistance.nded to check the latest documentation for the most accurate information.*
