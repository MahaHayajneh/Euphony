# Euphony: Context-Aware Audio Management Tool

## 1.0 Introduction

### Problem
Current headphones block ambient noise, which can be unsafe in outdoor environments. Euphony aims to provide context-aware audio management to enhance user safety by recognizing critical environmental sounds like alarms or a baby’s cry.

### Objective
Euphony uses environmental sensors and machine learning algorithms to offer adaptive sound recognition. It allows users to customize sound recognition settings for safety and enhanced audio experiences.

---

## 1.1 Need Analysis & Description

- **Need:** Traditional headphones lack the ability to balance immersion and awareness of important external sounds.
- **Solution:** Euphony integrates with existing headphones to provide real-time sound recognition, focusing on critical sounds like baby cries.

---

## 1.2 Project Constraints

### Technical Constraints
- Hardware compatibility with existing headphones.
- Real-time processing and low battery usage.

### Data Constraints
- Limited dataset availability for sound categories like baby cries, choking, and alarms.
- Ensuring high-quality, annotated datasets.

### User Constraints
- Simple, customizable interface.
- Protecting user privacy regarding audio data.

---

## 1.3 System Environment

### Hardware
- Environmental sensors (microphones).
- Mobile devices (smartphones/tablets).
- Existing headphones.

### Software
- PortAudio, Librosa, Pycaw, TensorFlow.

---

## 4.0 System Implementation

### 4.1 Methodology Pipeline

- **Data Preprocessing:** Noise reduction and audio augmentation.
- **Feature Extraction:** Mel-frequency cepstral coefficients (MFCC).
- **Model:** Convolutional Neural Network (CNN) for classification.

---

### 4.2 Technical Description

- **Preprocessing:** Noise reduction and data augmentation.
- **Model Training:** CNN model for sound classification with performance metrics (accuracy, MSE, precision).
- **Prediction:** Model detects baby cry and adjusts volume based on duration.

---

### 4.3 Data
- **Crying Baby Dataset:** 1200 audio files (from GitHub).
- **Others Dataset:** 1600 audio files (from UrbanSound8K).
- **Preprocessing:** Noise reduction, augmentation, and label assignment.

---

### 4.4 Feature Extraction
- **MFCC:** Extracted using Librosa for structured input to the machine learning model.

---

### 4.5 User Modeling
- **CNN Architecture:** Includes Conv2D, MaxPooling2D, and Dense layers.
- **Training Parameters:** Batch size 32, 50 epochs, Adam optimizer, binary cross-entropy.

---

### 4.6 Adaptation Techniques

- **Real-Time Audio Detection:** Using sounddevice library.
- **Dynamic Volume Control:** Adjusts audio volume based on baby cry duration.

---

## 5.0 Experimental Results

### 5.1 Performance Measures
- **Metrics:** Accuracy, Loss, MSE, Precision.

### 5.2 Results
- **Validation:** Accuracy: 0.9728, Precision: 0.9756, Loss: 0.1812, MSE: 0.0254.

---

### 5.3 Adaptation Effects
- **Volume Adjustment:** 20% reduction if cry lasts <30s; mute after 3 minutes.

---

## 6.0 Conclusions & Future Work

### Strengths
- High accuracy in sound classification.
- Robust dataset integration.

### Future Work
- Expand dataset for broader sound recognition.
- Improve real-time processing and power consumption.

