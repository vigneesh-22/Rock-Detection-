# YOLO Rock Detection

A real-time rock detection system using **Ultralytics YOLO** and **OpenCV**. The trained model detects rocks/stones from a live webcam feed and displays bounding boxes around detected objects.

## Project Description

* **Task:** Object Detection
* **Model:** Ultralytics YOLO
* **Classes:** Rock/Stone
* **Input:** Live webcam feed
* **Output:** Bounding boxes with detection results

The project focuses on detecting the presence and location of rocks rather than classifying different rock types.

## Project Structure

```text
Rock-Detection/
├── README.md
├── auto_label.py
└── best.pt
```

## How It Works

```text
Webcam
   ↓
OpenCV captures frame
   ↓
YOLO model
   ↓
Rock detection
   ↓
Bounding box
   ↓
Live display
```

The trained YOLO model processes each frame from the webcam. When a rock is detected, a bounding box is drawn around the detected object.

## Technologies Used

* Python
* Ultralytics YOLO
* OpenCV
* YOLO Object Detection

## Model

The trained model is stored as:

```text
best.pt
```

The model is loaded using Ultralytics:

```python
from ultralytics import YOLO

model = YOLO("best.pt")
```

## Installation

Install the required Python packages:

```bash
pip install ultralytics opencv-python
```

## Run the Project

Run:

```bash
python3 auto_label.py
```

The program opens the default webcam and performs real-time rock detection.

Press:

```text
q
```

to stop the detection window.

## Detection

The program:

1. Opens the default webcam.
2. Captures video frames using OpenCV.
3. Sends each frame to the YOLO model.
4. Detects rocks/stones.
5. Draws bounding boxes around detected objects.
6. Displays the live detection result.

## Applications

This type of rock detection can be useful for:

* Rover applications
* Robotics
* Terrain analysis
* Obstacle detection
* Autonomous exploration

## Future Improvements

* Improve detection accuracy with a larger dataset
* Add support for rover-mounted cameras
* Integrate the detector with ROS 2
* Deploy the model on an edge device
* Use detections for rover navigation
* Optimize inference for real-time embedded systems

## Learning Purpose

This project was developed as a hands-on learning project in **computer vision, YOLO object detection, OpenCV, model inference, and robotics applications**.
