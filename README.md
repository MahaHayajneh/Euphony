# Euphony 

## Introduction  
Welcome to **Euphony**, where technology meets empathy in decoding the emotional language of baby cries. **Euphony** is more than just a project—it's a mission to empower parents by transforming the complex language of infant cries into actionable insights. Through our mobile application, we aim to strengthen the bond between parents and babies, ensuring that no cry goes misunderstood.

---

## Project Timeline  
- **Start Date:** 8th March 2024  
- **End Date:** 25th May 2024  

---

## Need Analysis and Description  
Meet **Maya**, our primary user persona: a first-time mother experiencing the challenges of parenthood. Maya struggles to understand her baby’s cries, often feeling stressed and uncertain. She needs a reliable, non-intrusive mobile application that can interpret these cries in real-time, helping her feel more confident and providing peace of mind throughout her parenting journey.

---

## Project Constraints  
During development, we encountered the following challenges:
- **Limited Dataset:** The initial small dataset of baby cries required extensive preprocessing and feature extraction to ensure accuracy.
- **Time Constraints:** We had to balance efficient data collection, classification, and development within a tight timeframe.

---

## System Environment  
**Euphony** is designed as a mobile application compatible with both iOS and Android devices:

### Key Features:
- Real-time cry analysis
- Intuitive user interface for easy recording and interpretation of baby cries

---

## Project Software and Hardware Requirements  

### Software:
- **GUI Design:** Figma  
- **Programming Language:** Python (using libraries such as Keras and Librosa for machine learning and audio processing)

### Hardware:
- **Smartphone with Microphone:** Essential for recording baby cries  
- **Internet Connection:** Required for app installation, updates, and continuous model improvements  

---

## Research Background and Related Works  
The project draws from several studies on infant cry classification using machine learning techniques. We focused on:
- Exploring various models and techniques for effective cry classification
- Utilizing features like MFCC, spectrograms, and CNNs for accurate recognition

---

## Proposed Methodology  

### Pipeline of the Proposed Methodology:  
The development process involves:
1. Data collection and preprocessing
2. Feature extraction (MFCC, Mel Spectrogram, Chroma, Spectral Contrast)
3. Model training using a 1D Convolutional Neural Network (CNN)
4. Evaluation and deployment of the trained model

### Technical and Implementation Details:  
- **Dataset:** The **Donate a Cry Corpus** dataset from GitHub
- **Feature Extraction:** Using Librosa for audio feature extraction
- **Model:** Training a CNN model on extracted features for cry classification
- **GUI Development:** User-friendly interface designed with Figma and implemented with Python

### Dataset Description:  
- **Categories:** ‘Needs Burping’, ‘Belly Pain’, ‘Being Tired’, ‘Being Discomfort’, ‘Being Hungry’  
- **Preprocessing:** Cleaned and preprocessed to optimize feature extraction  

### Data Preprocessing:  
Minimal preprocessing required, focusing on:
- Ensuring mono audio samples for consistency
- Seamlessly transitioning to feature extraction

### Feature Extraction:  
Multiple features were utilized, including:
- MFCC
- Mel Spectrogram
- Chroma
- Spectral Contrast
- Tonnetz  
This enhanced the model’s performance by providing rich audio representations.

### Feature Selection:  
Top features were selected using SelectKBest with ANOVA F-value scoring, optimizing model efficiency for better results.

### Features Classification:  
A 1D CNN model was implemented:
- Sequential model with convolutional and pooling layers
- Trained using Adam optimizer, batch size of 64, for 100 epochs

---

## Experimental Results and Analysis  

### Performance Measures:  
- **Accuracy:** 86.09% on validation set  
- **Loss:** 0.3185 on validation set

### Experimental Results:  
The CNN model performed robustly, showing high accuracy and low loss during training and validation. However, challenges in generalization were noted, which will be addressed in future iterations.

---

## Conclusions and Future Works  

### Strengths:  
- **High Accuracy:** Achieved solid results despite the limitations of the initial dataset.
- **Effective Feature Extraction:** Features like MFCC and Mel Spectrogram provided the necessary representation for accurate classification.

### Weaknesses:  
- **Dataset Size:** A larger and more diverse dataset is needed to improve generalization.
- **Label Accuracy:** Expert validation of dataset labels will improve accuracy.

### Future Works:  
- Expand the dataset for enhanced performance
- Collaborate with domain experts for dataset validation and augmentation
- Develop a real-time application for continuous monitoring and cry analysis

---

## Conclusion  
**Euphony** harnesses the power of machine learning to decode the language of baby cries, paving the way for improved parent-child interactions. The project showcases how AI can address fundamental challenges in childcare, providing parents with tools to understand and respond to their baby’s needs with confidence.

--- 
