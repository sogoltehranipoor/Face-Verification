# Face-Verification
A deep learning-based Face Verification System that compares two face images and determines whether they belong to the same person.
Project Overview

Instead of directly classifying a person's identity, this project learns a feature representation (embedding) for each face image. The embeddings of two input images are then compared to determine their similarity.

The system can therefore perform:

Face Image 1 + Face Image 2 → Feature Comparison → Same Person / Different Person

Architecture

The project contains two main models:

1. Face Encoder

face_encoder.keras

The face encoder extracts meaningful features from an input face image and converts the image into a learned feature representation.

2. Face Verification Model

celeba_siamese_face_verification.keras

The verification model processes two face images and compares their learned representations to determine whether they belong to the same person.

Dataset

The project uses the CelebA (CelebFaces Attributes) Dataset, which contains a large collection of face images.

Main Concepts
Face Verification
Face Recognition
Feature Extraction
Face Embeddings
Siamese Neural Networks
Deep Learning
Computer Vision
Similarity Comparison
Technologies
Python
TensorFlow
Keras
NumPy
OpenCV
CelebA Dataset
Model Files
models/
│
├── face_encoder.keras
└── celeba_siamese_face_verification.keras
Workflow
Input Face A ──► Face Encoder ──► Embedding A ──┐
                                                 ├──► Similarity ──► Verification
Input Face B ──► Face Encoder ──► Embedding B ──┘

The system compares the feature representations generated from the two input images rather than relying only on raw pixel-level similarity.

Applications

Face verification systems can be used in applications such as:

Identity verification
Access control
Authentication systems
Security applications
Biometric systems
Future Improvements

Possible extensions include:

Real-time webcam face verification
Improved face alignment and preprocessing
Threshold optimization
Evaluation using ROC and AUC
Testing with additional face datasets
Deployment as a web application
