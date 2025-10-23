# Intelligent Traffic Violation Detection System

This project implements an Intelligent Traffic Violation Detection System using YOLOv5 for real-time object detection.
The system identifies motorcyclists, helmet usage, and vehicle number plates, enabling automated detection of traffic violations such as riding without a helmet.

## Objectives

- Detect riders and helmets in live or recorded video feeds.
- Identify traffic rule violations (no helmet).
- Detect and extract vehicle number plates for violator identification.
- Generate and store detection results for further analysis.

## Key Features

- Real-time detection using YOLOv5 deep learning model.
- Multi-object recognition: rider, helmet, and number plate.
- Violation detection logic (rider without helmet).
- Output video generation with bounding boxes and violation highlights.
- Modular, extendable Jupyter notebook for training and inference.

## Technologies Used
### Programming Language
Python 3.x
### Libraries & Frameworks
- YOLOv5 (PyTorch)
- OpenCV – image & video processing
- Pandas, NumPy – data handling
- Matplotlib – visualization
- Torch, Ultralytics – model operations
### Tools
- Jupyter Notebook – experimentation and visualization
- VS Code – development environment
- Git & GitHub – version control and project management

## 📁 Project Structure
```
traffic_violation/
│
├── yolov5.ipynb        # Main YOLOv5 training & detection notebook
├── .gitignore                   # Ignored files (e.g., runs/, __pycache__/)
├── README.md                    # Project documentation
│
├── ITDV/                        # Main project directory
│   ├── Dataset/                    # Dataset folder (images, labels)
│   │   ├── train/               # Training images & annotations
│   │   ├── val/                 # Validation images & annotations
│   │
│   ├── Output/                  # Model outputs (detections, results)
│   │   └── __results__files/    # Exported detection results
│   │
│   └── requirements.txt         # Project dependencies

```

## How It Works
### 1. Data Preparation
- Images of riders, helmets, and vehicles collected from traffic footage.
- Annotation done using tools like LabelImg for bounding boxes.
- Data organized into train and val directories.

### 2. Model Training
- Custom YOLOv5 model trained on annotated dataset.
- data.yaml defines dataset paths and class names.
- Fine-tuned for optimal performance using transfer learning.

### 3. Detection & Violation Identification
- Input video frames processed via trained YOLOv5 model.
- Logic identifies:
-- Rider detected
-- Helmet not detected
-- Violation flagged
- Results visualized with bounding boxes and saved videos.

### 4. Result Storage
- Detection images/videos saved to /Output/runs/detect/.
- Summary of violations logged for record-keeping or database integration.


## Results Summary
| **Metric**      | **Value** |
| --------------- | --------- |
| mAP@0.5         | 0.91      |
| Precision       | 0.88      |
| Recall          | 0.85      |
| FPS (Real-Time) | ~25       |


## Dependencies
- Install required libraries using:
```
pip install -r requirements.txt
```
- Or manually:
```
pip install torch torchvision opencv-python pandas matplotlib ultralytics
```

## Author
```
Nasira Kousar
Traffic Violation Detection Project | 2025
```
