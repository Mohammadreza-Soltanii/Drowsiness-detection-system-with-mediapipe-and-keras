# Drowsiness-detection-system-with-mediapipe-and-keras
A real-time driver drowsiness detection system using CNN (Keras) and MediaPipe Face Mesh.

# Real-Time Drowsiness Detection System using CNN & MediaPipe

This project is an intelligent, real-time drowsiness detection system designed for drivers and operators. By combining a Convolutional Neural Network (CNN) with MediaPipe Face Mesh, the system detects whether the user's eyes are open or closed via a webcam feed and triggers an alert if signs of fatigue are detected.

## 🚀 Key Features
- **High Accuracy (96.4%):** The model achieves high performance on validation data after only 5 epochs of training.
- **Smart Eye Isolation (MediaPipe Face Mesh):** Instead of processing the entire video frame, the system dynamically locates eye landmarks and crops only the eye regions for prediction.
- **Real-Time Inference:** Smooth, low-latency deployment utilizing OpenCV for immediate webcam stream processing.

## 📊 Model Architecture
The network is built using the Keras Sequential API with the following pipeline:
- **Conv2D Layer:** 32 filters to extract core visual features from the cropped eye images.
- **MaxPooling2D Layer:** For downsampling and reducing spatial dimensions.
- **Flatten & Dense Layers:** A fully connected block leading to a final Softmax layer for 2-class classification (`sleepy` vs. `awake`).

## 📦 Dataset
The model was trained on the well-known **MRL Eye Dataset** from Kaggle, which contains thousands of high-resolution eye images under various lighting conditions.

## 🛠 Tech Stack
- Python 3.12
- TensorFlow / Keras
- OpenCV (cv2)
- MediaPipe
- NumPy
