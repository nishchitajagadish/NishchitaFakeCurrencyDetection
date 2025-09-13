# FakeCurrencyDetection-Project
AI-powered solution to detect counterfeit Indian rupee notes using computer vision and deep learning.

---

## Overview
This project provides a practical tool for detecting counterfeit Indian currency using a combination of traditional image processing and modern deep learning frameworks. Built with **Python 3, OpenCV, TensorFlow, and Keras**, it extracts key visual features from banknotes to distinguish between genuine and fake notes.

---

## Motivation
India’s economy relies heavily on cash transactions, making the circulation of fake notes a serious concern—especially in areas where rigorous checks are not always feasible.  
The goal of this project is to empower small vendors, retailers, and everyday users with a quick, accessible method to verify currency authenticity using just a smartphone or webcam.

---

## Features
- **Denomination Detection**: Uses **OpenCV ORB** feature matching to identify the correct currency note (20, 50, 100, 500 INR).  
- **Fake vs Real Classification**: Implements **VGG16-based transfer learning** with image augmentation for robust classification.  
- **Image Preprocessing**: Resizing, grayscale conversion, thresholding, and edge detection to enhance accuracy.  
- **Training Insights**: Includes `loss.png` to visualize model training performance.  
- **Flexible Usage**: Supports both batch testing and single-image detection.  

---

## Dataset
- Contains **1200+ images** of Indian currency, categorized into `fake` and `real`.  
- Split into training, validation, and test sets for model development and evaluation.  

---

## Methodology
1. **Image Preprocessing**: Enhance quality and extract features using custom utilities (`utils.py`).  
2. **Denomination Detection**: ORB keypoint detection and brute-force matching using OpenCV.  
3. **Fake Currency Detection**: Transfer learning with VGG16. Images augmented with rotations, flips, brightness changes, and shifts to improve generalization.  
4. **Output**: Matched denominations are displayed with keypoints, and fake/real classification is provided for each note.  

---

## Challenges Faced
- Tuning hyperparameters such as the number of epochs was crucial to avoid overfitting or underfitting. Adjustments improved validation accuracy and model performance.  

---

## Results
- Successfully detected denominations with ORB feature matching.  
- Classified fake vs real notes with high accuracy using VGG16-based transfer learning.  
- Robust against variations in lighting, rotation, and scaling.  

---

## Usage

1. **Clone the repository:**
```bash
git clone <your-repo-url>


2. Install dependencies:

pip install -r requirements.txt

3. Run denomination detection:

python detect.py

4. Run fake currency detection:

python fakedet.py
