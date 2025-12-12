#  Multi-Object Detection in Surgical Instrument Trays Using YOLOv8
### CE888 Resit

##  Project Overview
This repository contains the complete implementation for detecting four surgical instruments in high-resolution tray images using the YOLOv8n deep learning model. The project follows the exact methodology described in the final report and includes dataset preprocessing, JSON-to-YOLO annotation conversion, training, evaluation, and exporting predictions in JSON format required by FASER.

##  Objective
Detect four surgical tools:
1. Bistoury
2. Dissection Forceps
3. Straight Scissors
4. Curved Scissors

##  Repository Structure
```
├── data/
├── annotations/
├── scripts/
├── models/
├── predictions/
└── README.md
```

##  Dataset Description
- Original dataset: 3,009 images  
- Sample used: 1,000  
- Split: 800 train / 100 val / 100 test  
- JSON annotations converted to YOLO format.
- https://drive.google.com/drive/folders/1YAEKgt4cTE_5YDX9SzTe2bcPda9zU0Fm?usp=drive_link
##  Installation
```
pip install ultralytics opencv-python numpy matplotlib tqdm
```

##  1. Convert JSON Annotations
```
python scripts/convert_json_to_yolo.py
```

##  2. Train YOLOv8n
```
python scripts/train_yolov8.py
```

##  3. Evaluate
Validation results from report:
- mAP@0.5 = 0.130  
- mAP@0.5:0.95 = 0.0827  

##  4. Export JSON Predictions (Required for FASER)
```
python scripts/export_predictions.py
```

##  Insights
Strengths, limitations, and future work described in the report.

##  Author
Sateesh V

