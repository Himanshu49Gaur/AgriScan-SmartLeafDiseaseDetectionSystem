# AgriScan – AI-Powered Bilingual Plant Disease Detection System

AgriScan is an edge-based agricultural intelligence system designed to detect plant diseases from leaf images and provide actionable, structured insights in both English and Hindi.

Unlike conventional plant disease classifiers that output only a predicted label, AgriScan functions as a knowledge-enriched decision support system built for real-world agricultural deployment.

---

# Executive Summary

AgriScan enables farmers and agricultural stakeholders to:

- Capture a photo of a plant leaf using a mobile device
- Detect disease instantly using a trained deep learning model
- Receive structured scientific information about the disease
- Understand causes, symptoms, treatment, prevention, and economic impact
- Access results in Hindi or English
- Operate fully offline with local inference

The system integrates:

- A trained deep learning model (TensorFlow/Keras)
- ONNX-based optimized local inference
- A bilingual JSON-driven knowledge engine
- A mobile-first APK application built with TypeScript, JavaScript, and CSS

---

# Problem Statement

Crop diseases significantly impact agricultural productivity, particularly in regions where:

- Farmers lack immediate access to agronomists
- Scientific information is not readily accessible in local languages
- Internet connectivity is unreliable
- Most available tools are either cloud-dependent or English-only

Many academic and Kaggle-style machine learning projects focus solely on classification accuracy without addressing real-world deployment, accessibility, or advisory depth.

AgriScan bridges this gap by combining AI-based detection with structured agricultural intelligence in an offline-capable system.

---

# Proposed Solution

AgriScan implements a complete edge-AI diagnostic pipeline:

1. User captures or uploads a leaf image  
2. Image is resized and normalized locally  
3. ONNX model performs inference on-device  
4. Predicted class and confidence score generated  
5. Disease metadata retrieved via bilingual JSON mapping  
6. Results rendered with severity indication and advisory guidance  

All processing occurs locally without any server or API dependency.

---

# System Architecture

## High-Level Workflow

| Step | Component                     | Description                                                                 |
|------|--------------------------------|-----------------------------------------------------------------------------|
| 1    | Camera / Image Upload         | User captures a leaf image using device camera or uploads from gallery.   |
| 2    | Image Preprocessing           | Image resized to 128×128 and normalized before inference.                  |
| 3    | ONNX Model Inference          | Optimized ONNX model performs local prediction on the device.              |
| 4    | Class Prediction + Confidence | Model outputs predicted disease class along with confidence score.         |
| 5    | JSON Knowledge Engine         | Disease metadata retrieved from bilingual (English/Hindi) JSON mapping.    |
| 6    | Bilingual UI Rendering        | Final results displayed with severity, advisory, and language selection.   |


---

## Architecture Components

### 1. Mobile Application Layer
- TypeScript
- JavaScript
- CSS
- APK-based deployment
- Camera integration
- Image upload functionality

### 2. Machine Learning Layer
- Custom CNN model (TensorFlow/Keras)
- Model saved as `.h5`
- Converted to ONNX format
- Local inference execution

### 3. Knowledge Engine
- Structured JSON-based disease database
- English and Hindi content mapping
- Dynamic rendering based on language selection

### 4. UI/UX Layer
- Confidence score display
- Severity classification (e.g., Moderate, Severe)
- Disease explanation sections
- Profile and scan statistics
- Language toggle system

---

# Machine Learning Pipeline

## Dataset

- Source: PlantVillage (Tomato subset)
- Total Classes: 10 (9 diseases + 1 healthy)
- Approximate Dataset Size: 18,000+ images
- Balanced class distribution
- **Source**: [Kaggle](https://www.kaggle.com/datasets/ashishmotwani/tomato)
- **Description**: The dataset contains over 20,000 images of tomato leaves with 10 diseases and 1 healthy class. Images are collected from both lab scenes and in-the-wild scenes.
- **Goal**: The objective is to develop a lightweight model that can predict tomato leaf disease and be deployed offline on a mobile app.


## Data Split

- Training: 80%
- Validation: 20%

## Image Preprocessing

- Resize: 128 × 128
- Pixel normalization: image / 255.0
- Data augmentation:
  - Rotation
  - Width shift
  - Height shift
  - Horizontal flip
  - Zoom

---
