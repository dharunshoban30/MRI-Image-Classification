# 🧠 Brain Tumour MRI Image Classification using Deep Learning
 
## Overview

This project is the implementation and evaluation of four Convolutional Neural Network (CNN) models for classifying brain tumours using MRI images. The project was conducted as part of a study on the application of deep learning techniques in medical imaging, aiming to improve the classification accuracy of various brain tumour types, including **Glioma, Meningioma, Pituitary Tumours, and No Tumour.** The datasets were obtained from Kaggle.

## Project Details 

1. **Project Objective:**

   The primary goal of this project is to design and evaluate CNN models that can effectively classify brain tumours from MRI images, providing an automated diagnostic tool to assist radiologists in identifying tumour types and planning treatments.

2. **Project Motivation:**

   Brain tumours account for 85-90% of primary central nervous system tumours and present significant diagnostic challenges due to their complex characteristics. Accurate classification of tumour types is crucial for determining effective treatment plans. This project leverages the power of Convolutional Neural Networks to enhance diagnostic efficiency, potentially leading to earlier and more accurate diagnosis.

3. **Models Implemented:**
   Four CNN models were implemented and evaluated:
   - **Custom 3-Layer CNN:** A basic CNN with three convolutional layers designed for extracting hierarchical features from MRI images.
   - **Custom 9-Layer CNN:** A deeper CNN architecture designed to capture complex patterns for more challenging classification tasks.
   - **VGG16:** A pre-trained CNN model known for its powerful feature extraction capabilities, often used in image classification tasks.
   - **VGG19**: A deeper variant of the VGG16 model, with additional layers for enhanced feature extraction.

   Each model was trained on the same dataset and evaluated using standard metrics like **Accuracy, Precision, Recall, and F-Score.**

## Methodology

The classification process involved several steps:

1. **Data Preprocessing:**
   - **Noise Reduction:** Applied Gaussian Blur to reduce noise in MRI images.
   - **Histogram Equalization:** Used Contrast Limited Adaptive Histogram Equalization (CLAHE) to enhance image contrast.
   - **Thresholding:** Converted images to binary format to segment the tumour region.
   - **Conversion and Normalization:** Converted images to RGB format and normalized pixel values to improve compatibility with neural networks.

2. **Model Training and Evaluation:**
   Each CNN model was designed and trained using the preprocessed MRI images. Key architectural details for each model are summarized below:
   - **3-Layer CNN:**
     - 3 Convolutional Layers followed by MaxPooling.
     - Flatten layer followed by 2 Dense layers.
     - SoftMax activation for classification.

   - **9-Layer CNN:**
     - 9 Convolutional Layers with MaxPooling after each layer.
     - Two fully connected layers for enhanced feature abstraction.
     - SoftMax activation for classification.
       
   - **VGG16 and VGG19:**
     - Pre-trained convolutional layers frozen to retain existing feature extraction capabilities.
     - Added custom dense layers for final classification.
     - SoftMax activation for classification.
      
## Setup Instructions
To execute the code, follow these steps:
1. **Setup Environment**:
    - Ensure you have Python and Jupyter Notebook installed.
    - Install necessary libraries using the following commands:
      ```bash
      pip install numpy pandas matplotlib scikit-learn
      ```

2. **Download Dataset**:
    - Ensure the `Training` and `Testing` folders are available in the same directory as the codes.

3. **Running the Codes**:
    - Open Jupyter Notebook and navigate to the `Project_Codes` file.
    - Run all the cells sequentially to see the workflow and the results.

 ## References
 - Dataset: [Kaggle Brain Tumor Classification (MRI)](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri?select=Training)
