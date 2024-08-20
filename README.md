# Drone Detection using YOLOv8

## How this model works:

![output](https://github.com/user-attachments/assets/58093d17-ef66-436a-9caa-995d7c68a8d8)
![output1](https://github.com/user-attachments/assets/6133736b-c966-4d8c-92fa-da9fac99b12e)
![output2](https://github.com/user-attachments/assets/416569ec-ce5b-454d-8917-8f0eca8e8711)

## Project Overview

This project focuses on detecting drones in video streams and images using the YOLOv8 model. The project includes training a YOLOv8 model on a publicly available dataset from Kaggle and performing real-time detection on video frames. The goal is to identify and highlight drones in each frame, making it useful for applications such as surveillance, airspace monitoring, and security.

## Project Workflow

### 1. **Environment Setup**

- Install necessary Python libraries including OpenCV, PyTorch, Ultralytics YOLO, and others.
- Download or clone the repository and set up the project directory.

### 2. **Model Initialization**

- Load a pre-trained YOLOv8 model (`yolov8n.pt`) using the Ultralytics library.
- Set the random seed for reproducibility.

### 3. **Dataset**

- The project uses the [YOLO Drone Detection Dataset](https://www.kaggle.com/datasets/muki2003/yolo-drone-detection-dataset/data) available on Kaggle.
- Download and prepare the dataset, ensuring it is structured correctly with images and YOLO-formatted labels.

### 4. **Model Training**

- Train the model using the Kaggle dataset specified in the `data.yaml` file.
- The training is configured to run on a GPU (if available) for 5 epochs, with model weights saved periodically.

### 5. **Image Detection**

- The trained model is used to predict and visualize drone detections on a set of test images.
- The predictions are displayed with bounding boxes indicating detected drones.

### 6. **Video Detection**

- Load a video file (e.g., `cam1.mp4`) and process it frame by frame.
- Convert each frame to the appropriate color format, perform detection, and then display the results in real-time.
- The video display updates with bounding boxes around detected drones.

### 7. **Model Saving**

- After training, the model can be saved for future use.
- The saved model can be reloaded later to perform detections without retraining.

## Project Structure

- `data.yaml`: Configuration file specifying the dataset paths and class names for training.
- `main.ipynb`: Jupyter notebook for model training, experimentation, and testing.
- `output1.png`, `output2.png`: Example output images showing drone detection results.
- `yolov8n.pt`: Pre-trained YOLOv8 model weights.
- `README.md`: Project documentation (this file).
