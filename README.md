# Deep Learning vs. Machine Learning: A Performance & Explainable AI Comparison for Fungal Infection Classification  

## Overview  

This project presents a comparative study of **traditional machine learning algorithms** (SVM, Random Forest, XGBoost) with **deep learning (ResNet50)** for fungal infection image classification.  
Alongside performance benchmarking, the project integrates **Explainable AI (Grad-CAM)** to visualize and interpret model predictions, ensuring transparency and reliability of AI-based fungal diagnosis.  

## Motivation  

Fungal infections are difficult to classify manually due to morphological similarity and time-consuming diagnostic methods. Leveraging AI-based image classification can improve both speed and accuracy, while explainability helps build trust with clinicians and researchers.  

## Dataset  

- **Name:** DeFungi Dataset  
- **Source:** [UCI Machine Learning Repository](https://doi.org/10.48550/arXiv.2109.07322)  
- **Classes:** H1, H2, H3, H5, H6 (microscopic images of fungi)  

**Preprocessing:**  
- Balanced dataset: 2,500 images per class (undersampling + augmentation)  
- Resized to 224×224 pixels  
- RGB → Grayscale for ML pipelines  

## Methods  

### Machine Learning Pipeline  
- **Feature Extraction:** Local Binary Patterns (LBP), Histogram of Oriented Gradients (HOG), and combined LBP+HOG  
- **Classifiers:** SVM, Random Forest, XGBoost  

### Deep Learning Pipeline  
- **Model:** ResNet50 (pre-trained on ImageNet)  
- **Automatic Feature Extraction:** Performed on RGB images  

### Explainable AI  
- **Grad-CAM** applied to ResNet50 to visualize which regions of the fungal images influenced predictions  

## Results  

- **ResNet50** outperformed all ML models, with accuracy increasing from **0.68 (500 images/class)** to **0.73 (2,500 images/class)**.  
- **XGBoost with LBP** performed best among ML models.  
- **Grad-CAM visualizations** showed biologically relevant regions being highlighted, confirming interpretability of deep learning predictions.  
