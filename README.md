# 🐱🐶 Audio Recognition using Fully Connected MLP

Binary Audio Classification: **Cats vs Dogs**

This project evaluates the performance of a Fully Connected Neural Network (MLP) for audio classification using different audio representations from a Kaggle dataset.

---

##  Objective

The goal of this project is to compare the performance of a **Fully Connected Neural Network (MLP)** using different audio feature representations:

- Time Domain
- Frequency Domain (FFT)
- Spectrogram
- Mel Spectrogram
- MFCC

Models are evaluated using:

- Accuracy
- F1 Score
- AUC

---

## 📂 Dataset

**Source:**  
[Kaggle – Audio Cats and Dogs](https://www.kaggle.com/datasets/mmoreaux/audio-cats-and-dogs)

### Dataset Composition

| Class | Files | Original Duration |
|-------|-------|------------------|
| Cats  | 164   | 1323.90 seconds |
| Dogs  | 113   | 598.44 seconds  |

### Audio Challenges
- Variable-length recordings (2s to >15s)
- Background noise
- Amplitude variability
- Signal quality differences
---

## 🔧 Data Preprocessing

### 1️. Silence Removal

Silence segments were removed to improve signal quality:

| Class | Original Duration | After Silence Removal |
|-------|-------------------|----------------------|
| Cats  | 1323.90 s         | 909.55 s             |
| Dogs  | 598.44 s          | 417.95 s             |

### 2️. Audio Segmentation

To ensure compatibility with MLP (which requires fixed-size inputs):

- Each audio file was divided into **3-second segments**
- Short segments were zero-padded
- Each segment saved as independent WAV

This guarantees consistent input dimensions.

---

## Model Architecture

Fully Connected Neural Network (MLP):

```

Input (D features)
↓
Dense (64 neurons, ReLU)
↓
Dense (32 neurons, ReLU)
↓
Output (1 neuron, Sigmoid)

```

- Loss: Binary Crossentropy
- Optimizer: Adam



## 📁 Project Structure

```

├── data/
├── notebooks
├── requirements.txt
└── README.md

---

## Author

Alessa Melo  
Universidad Yachay Tech  
School of Mathematical and Computational Sciences  
February 2026
```


