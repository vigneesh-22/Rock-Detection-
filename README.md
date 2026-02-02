 Rock Detection using YOLO:

This project implements a rock detection system using YOLO (You Only Look Once) object detection.
The model detects rocks in real-time from images or a live camera feed (webcam / rover-mounted camera).

The project focuses only on detecting the presence and location of rocks, not classifying rock types.

  Project Description
Task: Rock detection (object detection)
Model: YOLO (Ultralytics)
Classes: Rock (single class)
Input: Image / Live camera feed
Output: Bounding box with confidence score

 Methodology

YOLO is trained with a single class: rock
The model learns visual features such as:
Shape
Texture
Surface patterns
During inference, YOLO predicts:
1-Bounding box coordinates
2-Detection confidence

This approach enables fast and real-time rock detection, suitable for robotics and rover applications.


 Dataset Structure

yolo_dataset/
├── images/
│   ├── train/
│   └── val/
├── labels/
│   ├── train/
│   └── val/
└── data.yaml

Images captured using webcam / rover camera

Rocks annotated using bounding boxes

YOLO label format used



 Model Training

Framework: Ultralytics YOLO
Task: Object Detection
Number of Classes: 1 (rock)
Output Model File:
yolo_rock_detector.pt


  How to Run

Install dependencies:

pip install ultralytics opencv-python

Run detection:

python detect_rock.py

Press q to exit the camera window.


  Output

Bounding boxes drawn around detected rocks

Confidence score displayed on the frame


Example:

Rock (0.81)
