
# 📌 Hindi Handwritten Character Recognition using CNN

This project focuses on classifying handwritten Hindi (Devanagari script) consonants using Deep Learning. The system is built using Convolutional Neural Networks (CNNs) trained on a dataset of 36 unique character classes.

## 🧠 Problem Overview

Recognizing handwritten Hindi characters is challenging due to:

Variations in writing styles

Complex curves, strokes & modifiers (Matras)

Similar-looking characters

Limited benchmark datasets

This project aims to build a robust deep learning model capable of accurate Hindi character classification.

## 🗂 Dataset Used

Dataset Name: DHCD (Hindi Handwritten Character Dataset)

Classes: 36 Consonants

Image Size: 32 × 32 pixels

Color Mode: Grayscale

Preprocessed: Cropped, normalized & centered characters

## 🏗 Model Architectures

Two CNN architectures were designed and evaluated:

## ✅ Architecture 1 – Deep CNN (Baseline Model)
Layer	Configuration
Input	32×32×3
Conv2D	(64 filters, 3×3)
BatchNorm + Conv2D	(64 filters, 3×3)
MaxPooling	(2×2)
Conv2D	(128 filters, 3×3)
Conv2D + BatchNorm	(128 filters, 3×3)
MaxPooling	(2×2)
Conv2D	(256 filters, 3×3)
MaxPooling	(2×2)
Dense	512 units + ReLU
Dropout	0.4
Output Layer	36 units + Softmax

🔹 Optimizer: Adam
🔹 Test Accuracy: 96.40%

## ✅ Architecture 2 – Lightweight CNN (Optimized Model)
Layer	Configuration
Input	32×32×3
Conv2D	32 filters
Conv2D	64 filters
MaxPooling	(2×2)
Conv2D	128 filters
MaxPooling	(2×2)
Dense	128 units + ReLU
Dropout	0.3
Output Layer	36 units + Softmax

🔹 Optimizer: SGD with momentum (0.9)
🔹 Test Accuracy: 96.55% ✅ Best Model

## 🔍 Key Findings
Metric	Architecture 1	Architecture 2
Training Accuracy	98.31%	98.98%
Testing Accuracy	96.40%	96.55%
Loss (Test)	0.1272	0.1173
Parameters	High	Moderate

✔ Architecture 2 provides better generalization
✔ Less overfitting + lower complexity
✔ Suitable for deployment and real-time applications

## 🧰 Technologies Used
Category	Tools & Libraries
Programming Language	Python
Deep Learning Framework	TensorFlow / Keras
Image Processing	OpenCV
Visualization	Matplotlib, Seaborn
Dataset Handling	TensorFlow Data Pipeline
## 🎯 Applications

OCR for Hindi documents

Digital archival of handwritten content

Assistive tech for visually impaired users

Educational handwriting evaluation

Language digitization & preservation

## 🚀 Future Enhancements

Include vowels & compound characters

Support full word/sentence recognition

Improve real-time prediction performance

Mobile + Web deployment (TFLite)
