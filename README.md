Medical Imaging AI: Cancer Detection System(USING SYNTHETIC DATA)

Overview
This is a deep learning-based medical imaging analysis system designed to detect potential cancerous abnormalities in medical scans. The system uses synthetic data for training and provides a user-friendly interface for analyzing uploaded medical images.


How to Use the System

1.Upload an Image: Drag and drop or click to upload a medical scan (X-ray, MRI, CT, etc.)
2.Adjust Sensitivity: Use the slider to set detection sensitivity (higher values catch more potential cases but may increase false positives)
3.Click Analyze: The system will process the image and generate a diagnostic report
4.Review Results: Examine the risk assessment, visualization, and recommendations


Key Features

1. Advanced Image Processing:

Adaptive histogram equalization
CLAHE (Contrast Limited Adaptive Histogram Equalization)
Noise reduction
Automatic format conversion (handles grayscale, RGB, RGBA)



2. Deep Learning Model:

Based on MobileNetV3Small architecture for efficiency
Transfer learning from ImageNet weights
Custom classification head with regularization
Trained with class weighting for imbalanced data



3.Comprehensive Reporting:

Risk score (0-1 probability)
Risk level classification (Low/Moderate/High)
Confidence estimation
Personalized recommendations based on sensitivity



4. Visualization:

Side-by-side comparison of original and processed images
Enhanced view highlights potential abnormalities



5.Customization:

Adjustable sensitivity threshold
Detailed model information available





How It Was Built

1.Synthetic Data Generation:

Created realistic synthetic medical images with abnormalities
Simulated different tissue textures and lesion characteristics


2.Model Development:

Used transfer learning with MobileNetV3Small
Added custom dense layers with regularization
Implemented careful class weighting for the imbalanced dataset
Used multiple metrics (AUC, precision, recall) for evaluation


3.Training Process:

Learning rate scheduling
Early stopping based on validation AUC
Learning rate reduction on plateau
30 epochs of training with batch size 32


4.Deployment

Built with Gradio for easy web interface
Includes comprehensive error handling
All values converted to native Python types for compatibility





Technical Specifications

Framework: TensorFlow 2.12.0
Base Model: MobileNetV3Small
Input Size: 224×224 pixels
Processing: CLAHE + Adaptive Histogram Equalization
Output: Probability score (0-1) with risk assessment





> ⚠️ **Disclaimer**: This system is for **educational and demonstration purposes** only. It uses **synthetic data** and is **not intended for clinical use**.

---

## 🚀 Overview

Welcome to the **Medical Imaging AI** platform — a smart, deep learning-powered tool for identifying potential **cancerous abnormalities** in medical scans. Designed with an intuitive interface and a robust backend, it empowers users to visualize, analyze, and understand risk assessments — all in real time.

---

## ✨ Key Features

### 🧪 Advanced Image Processing
- ✅ Adaptive Histogram Equalization
- ✅ CLAHE (Contrast Limited Adaptive Histogram Equalization)
- ✅ Noise Reduction for Clarity
- ✅ Auto Support for RGB, RGBA, and Grayscale Formats

### 🧠 Deep Learning Model
- ⚙️ **MobileNetV3Small** backbone (efficient and accurate)
- 🏋️ Transfer learning from **ImageNet**
- 🔁 Custom classification head with **L2 regularization & dropout**
- ⚖️ **Class weighting** for imbalanced data

### 📋 Comprehensive Reporting
- 📊 **Risk Score**: (0 - 1 probability)
- 🟢🟡🔴 Risk Level: **Low**, **Moderate**, or **High**
- ✅ Confidence Estimation
- 💡 Personalized **recommendations**

### 🖥️ Interactive Interface
- 🎛️ Sensitivity Control Slider
- 🖼️ Original vs Processed Image Comparison
- 📈 Model performance metrics (AUC, precision, recall)




🧩 System Architecture

graph TD
    A[User Uploads Image] --> B[Image Preprocessing]
    B --> C[CLAHE + Histogram Equalization + Noise Reduction]
    C --> D[Model Inference (MobileNetV3Small)]
    D --> E[Risk Score + Classification]
    E --> F[Visualization & Recommendations]



⚠️ Limitations
❗ Important Notes:

📌 Uses synthetic training data only
❌ Not FDA/clinically approved
🚫 Not a substitute for professional diagnosis
🧪 Intended for education/demo use








