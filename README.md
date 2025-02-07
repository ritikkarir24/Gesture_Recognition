# **Gesture Recognition**

## **INDEX**
- [Potential Queries](#Potential_Queries)


## **Project Overview**

This project focuses on developing a gesture recognition system for smart TVs. The goal is to allow users to control the TV without a remote using five predefined gestures:

- **Thumbs Up:** Increase volume
- **Thumbs Down:** Decrease volume
- **Left Swipe:** Jump backward 10 seconds
- **Right Swipe:** Jump forward 10 seconds
- **Stop:** Pause the movie

Each video consists of 30 frames, and the system must process these frames to identify gestures accurately.

## **Objectives**

1. **Data Generator:** Efficiently handle batches of video data with preprocessing steps like cropping, resizing, and normalization.
2. **Model Development:** Build an accurate, parameter-efficient model for real-time gesture recognition.
3. **Documentation:** Detail the rationale behind model choices and the experimental process leading to the final model.

## **Technologies Used**

- **NumPy:** Efficient numerical operations for image arrays.
- **OpenCV (cv2):** Reading, resizing, and preprocessing video frames.
- **ImageIO & Scikit-Image:** Loading and transforming image data.
- **TensorFlow & Keras:** Building and training deep learning models.
- **Matplotlib:** Visualizing data and model performance.
- **GRU & LSTM:** Capturing temporal dependencies in video sequences.
- **Conv2D & Conv3D:** Extracting spatial and temporal features.
- **Model Callbacks:** Optimizing training with EarlyStopping and ReduceLROnPlateau.

## **Project Workflow**

### **1. Data Preprocessing**

- **Frame Extraction:** Extract 30 frames per video.
- **Resizing & Normalization:** Standardizes frame size and scales pixel values (0-1).
- **Batch Generator:** Handles data feeding efficiently during training.

### **2. Model Architecture**

- **Convolutional Layers (Conv2D/Conv3D):** Extract spatial and temporal features.
- **TimeDistributed Layer:** Applies convolutional operations across frames.
- **Recurrent Layers (GRU/LSTM):** Learn temporal patterns in sequences.
- **Dense Layers:** Perform final gesture classification.
- **Regularization:** Dropout and Batch Normalization reduce overfitting.

### **3. Training Strategy**

- **Model Checkpoints:** Save the best model based on validation accuracy.
- **Early Stopping:** Prevent overfitting by halting early.
- **Learning Rate Scheduling:** Dynamically adjust learning rate with ReduceLROnPlateau.

## **Potential Queries**

