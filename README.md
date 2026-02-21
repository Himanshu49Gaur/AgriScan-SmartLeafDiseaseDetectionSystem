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

