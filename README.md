# YOLO Rock Detection

A real-time rock detection system using **Ultralytics YOLO** and a custom single-class dataset. The system detects the presence and location of rocks in images and live camera feeds using bounding boxes and confidence scores.

## Project Description

* **Task:** Object Detection
* **Model:** Ultralytics YOLO
* **Classes:** 1 — Rock
* **Input:** Images / Live Camera Feed
* **Output:** Bounding boxes with confidence scores

This project focuses on detecting rocks rather than classifying different rock types.

## Methodology

The YOLO model is trained using a custom dataset containing a single class: `rock`.

During training, the model learns visual features such as:

* Shape
* Texture
* Surface patterns
* Visual appearance

During inference, YOLO predicts:

1. Bounding box coordinates
2. Detection confidence

The resulting detections can be used for real-time rock detection in robotics and rover applications.

## Dataset Structure

```text
yolo_dataset/
├── images/
│   ├── train/
│   └── val/
├── labels/
│   ├── train/
│   └── val/
└── data.yaml
```

The images were collected using a webcam and/or rover-mounted camera.

Rocks were manually annotated using bounding boxes following the YOLO annotation format.

## YOLO Label Format

Each rock annotation follows the YOLO format:

```text
class_id center_x center_y width height
```

All coordinates are normalized between `0` and `1`.

Since this project contains only one class:

```text
0 = rock
```

## Model Training

* **Framework:** Ultralytics YOLO
* **Task:** Object Detection
* **Number of Classes:** 1
* **Class:** Rock

### Trained Model

```text
yolo_rock_detector.pt
```

## Installation

Install the required dependencies:

```bash
pip install ultralytics opencv-python
```

## Run Detection

Run the detection program:

```bash
python detect_rock.py
```

The program can perform detection using a live camera feed.

Press:

```text
q
```

to exit the camera window.

## Output

The system displays:

* Bounding boxes around detected rocks
* Confidence score for each detection
* Real-time camera output

Example:

```text
Rock (0.81)
```

where `0.81` represents the model's confidence score for the detected rock.

## Applications

This rock detection system can be useful for:

* Rover navigation
* Robotic exploration
* Terrain analysis
* Obstacle detection
* Underground/mining robotics
* Autonomous robotic systems

## Future Improvements

* Detect multiple rock classes
* Improve detection accuracy with a larger dataset
* Deploy the model on an edge device
* Integrate detection with ROS 2
* Use detected rocks for rover navigation and obstacle avoidance
* Optimize the model for real-time embedded deployment

## Learning Purpose

This project was developed as a hands-on learning project for computer vision, object detection, dataset annotation, YOLO model training, and real-time inference.
