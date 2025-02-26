# 🎤 Real-Time Target Speaker Recognition

## 📌 Overview
This project implements a deep learning-based real-time target speaker recognition system using **CNN** and **Bi-Directional LSTM** models. It classifies audio samples as belonging to a **target speaker** or not, even in noisy environments.

## 🚀 Features
- **Deep Learning Models**: Bi-Directional LSTM and CNN architectures for classification.
- **Audio Feature Extraction**: Uses **MFCC, Delta-MFCC, and Delta-Delta MFCC** for analysis.
- **Dataset**: Extracted audio from [Deep Voice Dataset](https://www.kaggle.com/datasets/birdy654/deep-voice-deepfake-voice-recognition) + additional .wav files.
- **Real-Time Testing**: Supports real-time speaker classification.
- **Accuracy**: Achieved **90%** accuracy for target speakers and **87%** for non-targets.

## 📂 Dataset & Preprocessing
- **Target Speaker**: Taylor Swift
- **Non-Target Speakers**: Joe Biden, Donald Trump, Barack Obama, Elon Musk
- **Data Preparation**:
  - Audio clips of 10 minutes per speaker were split into 25-second segments.
  - Data split into **target**, **non-target**, and **test** folders.
  - Preprocessing includes **padding, truncation, augmentation, noise filtering**.

## 🏗 Model Architecture
- **Feature Extraction**: MFCC + Delta & Delta-Delta MFCC
- **Network**:
  - **Bi-Directional LSTM** layers
  - Fully connected layers for classification
- **Training Optimizations**:
  - **Early Stopping** to prevent overfitting
  - **Saved Model**: `voice_classifier_model.keras`

## 🛠 Setup & Installation
```bash
# Clone the repository
git clone https://github.com/Swini27/Real-Time-Target-Speaker-Recognition.git
cd Real-Time-Target-Speaker-Recognition

# Install dependencies
pip install -r requirements.txt
```

## 🔍 How to Use
### 1️⃣ Run Predictions on Test Audio
```python
from model import run_predictions
run_predictions("path/to/test/folder")
```
### 2️⃣ Real-Time Speaker Classification
```python
from model import listen_and_classify
listen_and_classify()
```

## 📊 Results
| Metric               | Score |
|---------------------|-------|
| **Target Accuracy** | 90%   |
| **Non-Target Accuracy** | 87%   |

## 🤝 Contributing
Feel free to **fork** this repo, make improvements, and create a **pull request**.

## 📜 License
This project is licensed under the **MIT License**.

---
Made with ❤️ by Harjot Singh 🚀
