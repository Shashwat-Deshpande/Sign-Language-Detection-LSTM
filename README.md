# Real-Time Sign Language Detection with LSTM

This project implements a real-time sign language detection system using a Long Short-Term Memory (LSTM) neural network. It captures video feed via a webcam, extracts holistic keypoints (face, hands, pose) using **MediaPipe**, and classifies sequences of gestures using a trained **TensorFlow/Keras** model.

## 🛠️ Tech Stack
- **Python** 3.x
- **OpenCV** (Computer Vision & Image Processing)
- **MediaPipe** (Keypoint Extraction)
- **TensorFlow / Keras** (LSTM Neural Network)
- **NumPy** (Data manipulation)

## 🚀 Features
- **Real-Time Detection:** Predicts gestures instantly from a webcam feed.
- **Holistic Tracking:** Tracks face, pose, and hand landmarks for robust detection.
- **Sequence Modeling:** Uses 30-frame sequences to understand the context of movement, distinguishing between static and dynamic signs.
- **Interactive UI:** Displays real-time probability bars and predicted text on screen.

## 📂 Project Structure
- `Sign_Language_Detection.ipynb`: The main notebook containing data collection, preprocessing, model training, and real-time prediction logic.
- `action.h5`: The trained model weights (saved after 300 epochs).

## 🎥 How It Works
1. **Data Collection:** The system captures 30 frames of keypoints for each action (e.g., "Hello", "Thanks", "I Love You").
2. **Preprocessing:** Keypoints are normalized and structured into sequences.
3. **Training:** An LSTM network trains on these sequences to learn temporal dependencies.
4. **Inference:** The model predicts the action in real-time with a confidence threshold.
