# 🧠 Brain Tumour MRI Image Classification using Deep Learning
 
## Overview
This project is the implementation and evaluation of four Convolutional Neural Network (CNN) models for classifying brain tumours using MRI images. The project was conducted as part of a study on the application of deep learning techniques in medical imaging, aiming to improve the classification accuracy of various brain tumour types, including **Glioma, Meningioma, Pituitary Tumours, and No Tumour.**

## Project Details 
1. **Project Objective:**

   The primary goal of this project is to design and evaluate CNN models that can effectively classify brain tumours from MRI images, providing an automated diagnostic tool to assist radiologists in identifying tumour types and planning treatments.

2. **Project Motivation:**

   Brain tumours account for 85-90% of primary central nervous system tumours and present significant diagnostic challenges due to their complex characteristics. Accurate classification of tumour types is crucial for determining effective treatment plans. This project leverages the power of Convolutional Neural Networks to enhance diagnostic efficiency, potentially leading to earlier and more accurate diagnosis.

3. **Possible Applications:**
   - Medical Diagnostics: Assists dermatologists in identifying and diagnosing skin lesions.
   - Telemedicine: Enables patients to upload images for preliminary analysis.
   - Research: Provides a tool for analyzing large datasets of skin lesion images for research purposes.
   - Mobile Apps: Can be integrated into smartphone applications for self-assessment.

## Methodology
The image segmentation approach uses a multi-step process involving several preprocessing, processing, and post-processing techniques. Below is a summary of the key steps:
  - **Image Conversion:** Convert the input image to grayscale using OpenCV (cv2.cvtColor()), which simplifies the processing by reducing the image to a single channel.
  - **Adaptive Thresholding:** Apply a combination of Otsu's thresholding and inverse binary thresholding to create a binary image where lesions are highlighted.
  - **Morphological Operations:** Use opening and closing operations to remove noise and refine the segmented areas.
  - **Area Segmentation:** Calculate sure foreground and background regions using distance transform and dynamic thresholding.
  - **Connected Component Labelling:** Assign unique labels to individual lesions using connected component analysis.
  - **Watershed Algorithm:** Apply the Watershed segmentation algorithm to distinguish between different regions in the image.
  - **Gaussian Blur:** Apply a Gaussian Blur to smooth the segmented regions for better visual appearance.

The main Python script for the image segmentation algorithm is contained in `imageSegment.py`, and the visualizations for each step are presented in the Jupyter notebook `visualSegment.ipynb`.

## Setup Instructions
To execute the code, follow these steps:
1. **Setup Environment**:
    - Ensure you have Python and your preferred IDE installed.
    - Install necessary libraries using the following commands:
      ```bash
      pip install numpy pandas matplotlib scikit-learn
      ```

2. **Download Dataset**:
    - Ensure the `dataset` folder is available in the same directory as the codes.

3. **Running the Codes**:
    - Open the IDE and navigate to the `visualSegment.py` file.
    - Run the file in the terminal to see the results.
    - To look at the visualizations, run all the cells in `imageSegment.py` notebook in the IDE or in Jupyter Notebook. 
