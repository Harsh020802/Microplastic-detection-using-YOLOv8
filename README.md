# Microplastic Detection with YOLO

An AI-powered microplastic detection system using YOLOv8 to identify microplastic particles in environmental samples and microscopic images.

## Features
- Microplastic particle detection
- Dataset validation for microscopic imagery
- Bounding box visualization for detected particles
- YOLOv8 model training optimized for small particle detection
- Roboflow integration for microplastic dataset management

## Quick Start
bash
pip install ultralytics roboflow numpy pandas pillow matplotlib


python
from ultralytics import YOLO

# Train model
model = YOLO("yolov8n.yaml")
model.train(data="data.yaml", imgsz=1280, batch=1, epochs=100)


## Dataset Structure

archive/
├── train/ (images + annotations.csv)
└── valid/ (images + annotations.csv)


CSV format: filename, width, height, xmin, ymin, xmax, ymax