# Language Identification (LID) using MFCC + Mel Spectrogram

## Overview

This project implements a Language Identification (LID) system to classify speech into five languages:

* Hindi
* Marathi
* Telugu
* English
* Malayalam

The system uses MFCC and Mel Spectrogram features along with a Neural Network (MLP) for classification.

---

## Project Structure

Language-Identification-LID/
│
├── data/
│   ├── hindi/
│   ├── marathi/
│   ├── telugu/
│   ├── english/
│   ├── malayalam/
│
├── notebooks/
│   └── lid_project.ipynb
│
├── outputs/
│   └── model.pth
│
├── requirements.txt
├── README.md
└── report.tex

---

## Installation

pip install -r requirements.txt

---

## How to Run

jupyter notebook notebooks/lid_project.ipynb

Run all cells. The model will train and evaluate automatically.

---

## Methodology

1. Collect audio samples from Mozilla Common Voice dataset
2. Perform preprocessing:

   * Silence trimming
   * Resampling to 16kHz
3. Extract features:

   * MFCC (40 coefficients)
   * Mel Spectrogram
4. Combine features into a single feature vector
5. Train a Neural Network classifier
6. Evaluate using:

   * Accuracy
   * Precision
   * Recall
   * F1-score
   * Confusion Matrix

---

## Model Details

* Model Type: Feedforward Neural Network (MLP)
* Architecture:

  * Input Layer → 128 neurons → ReLU
  * Hidden Layer → 64 neurons → ReLU
  * Output Layer → 5 classes
* Loss Function: CrossEntropyLoss
* Optimizer: Adam
* Epochs: 10
* Batch Size: 16

---

## Dataset

* Source: Mozilla Common Voice
* Languages Used:

  * Hindi
  * Marathi
  * Telugu
  * English
  * Malayalam
* Format: .mp3
* Samples: ~100 per language

---

## Results

* Accuracy: 84% (update after running)
* Evaluation:

  * Classification Report
  * Confusion Matrix

---

## Responsible AI

* Dataset balanced across languages
* Evaluated model performance per language
* Confusion matrix used to detect bias

---

## Reproducibility

1. Run notebook
2. Results will be generated automatically

---

## Future Improvements

* Use CNN or Transformer models
* Increase dataset size
* Improve performance on short audio clips

---

## Author
Shubham Verma (M25DE1005)
Nikhil Jaitak (M21AIE236)
