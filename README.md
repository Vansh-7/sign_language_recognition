# Real-Time American Sign Language Recognition System

**Author:** Vansh Gupta
**GitHub:** [https://github.com/Vansh-7/sign\_language\_recognition](https://github.com/Vansh-7/sign_language_recognition)
**Dataset:** [ASL Alphabet Dataset on Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)

---

## Overview

This project implements a lightweight, real-time American Sign Language (ASL) recognition system using MediaPipe for hand landmark extraction and a custom Multi-Layer Perceptron (MLP) model for gesture classification. The system operates efficiently on standard consumer hardware without the need for specialized sensors, providing live sign translation with audio feedback and a simple, user-friendly GUI.

---

## Features

* Real-time ASL alphabet recognition (29 signs) at 28-30 FPS
* Uses only a standard webcam and CPU (Intel i5 or equivalent)
* MediaPipe Hands for fast and accurate hand landmark detection
* Custom MLP model trained on the ASL Alphabet Dataset from Kaggle
* Text-to-speech feedback using `pyttsx3`
* Simple Tkinter-based GUI for easy interaction
* Save recognized signs to a text file

---

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Vansh-7/sign_language_recognition.git
   cd sign_language_recognition
   ```

2. Install required Python packages:

   ```bash
   pip install -r requirements.txt
   ```

3. (Optional) Ensure your system supports `pyttsx3` for text-to-speech functionality.

---

## Usage

Run the system by opening and executing the Jupyter Notebook file `asl_mediapipe_final.ipynb`.

Workflow:

* The webcam feed opens with real-time ASL sign prediction.
* Predicted signs display as text on-screen and are spoken aloud.
* Use the **Save** button to export recognized signs to a text file.

---

## Dataset

This project uses the ASL Alphabet Dataset by Grassknoted available on Kaggle:
[https://www.kaggle.com/datasets/grassknoted/asl-alphabet](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)

---

## Model Details

* Input: 63-dimensional vector (21 hand landmarks × 3 coordinates)
* Architecture: MLP with layers \[63-128-64-29], ReLU activations, dropout, and L2 regularization
* Training: AdamW optimizer, early stopping, label smoothing for generalization

---

## Results

* Achieved 94% classification accuracy on unseen test data
* Real-time performance at 28-30 FPS on consumer-grade laptops
* Robust performance in well-lit, uncluttered environments

---

## Future Work

* Extend to dynamic gesture recognition with temporal models (LSTM/Transformer)
* Mobile deployment with TensorFlow Lite
* Support for multiple sign languages (e.g., ISL, BSL)
* Integration with AR/VR devices for immersive assistive tech

---

## License

MIT License — see [LICENSE](LICENSE) for details.

---

## Contact

For questions or collaboration, contact Vansh Gupta via GitHub or email.
