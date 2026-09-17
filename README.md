# YOLO Rock Detection

A real-time rock detection project using **Ultralytics YOLO** and **OpenCV**. The trained YOLO model detects rocks from a live camera feed and displays bounding boxes with confidence scores.

## Features

* Real-time rock detection
* Live webcam input
* YOLO-based object detection
* Bounding boxes around detected rocks
* Detection confidence scores
* Single-class rock detection

## Technologies Used

* Python 3
* Ultralytics YOLO
* OpenCV
* YOLO Object Detection

## Project Structure

```text
Rock-Detection-/
├── README.md
├── auto_label.py
└── best.pt
```

## How It Works

```text
Webcam
   ↓
OpenCV
   ↓
Capture Video Frame
   ↓
YOLO Model
   ↓
Rock Detection
   ↓
Bounding Box + Confidence
   ↓
Display Detection
```

The webcam captures live video frames using OpenCV. Each frame is passed to the trained YOLO model, which detects rocks and draws bounding boxes around the detected objects.

## Model

The trained YOLO model is stored in:

```text
best.pt
```

The model is loaded using the **Ultralytics YOLO** framework.

## Installation

Clone the repository:

```bash
git clone https://github.com/vigneesh-22/Rock-Detection-.git
```

Move into the project directory:

```bash
cd Rock-Detection-
```

Install the required dependencies:

```bash
pip install ultralytics opencv-python
```

> It is recommended to use a Python virtual environment when installing the dependencies.

## Run the Project

Run the detection program:

```bash
python3 auto_label.py
```

The program will access the default webcam and perform real-time rock detection.

Press:

```text
q
```

to exit the detection window.

## Output

When a rock is detected, the model displays a bounding box around it along with the detection confidence.

Example:

```text
Rock (0.81)
```

Here, `0.81` represents the model's detection confidence.

## Applications

This project can be used as a basic computer vision component for:

* Robotics
* Rover applications
* Terrain analysis
* Obstacle detection
* Autonomous exploration
* Mining and underground robotics

## Future Improvements

* Improve detection accuracy using a larger dataset
* Support rover-mounted cameras
* Integrate with ROS 2
* Use detections for rover navigation
* Deploy the model on an edge device
* Optimize the model for real-time embedded systems

## Learning Purpose

This project was developed as a hands-on learning project to understand:

* YOLO object detection
* Computer vision
* OpenCV
* Model inference
* Real-time camera processing
* AI applications in robotics
