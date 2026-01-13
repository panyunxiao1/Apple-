# YOLOv11 Agricultural Object Detection

This repository provides code and scripts for object detection using Ultralytics **YOLOv11** in agricultural scenarios .

## Dataset

The complete annotated dataset is publicly available on Roboflow:  
**Dataset Link**: https://app.roboflow.com/yolo11-iv6di/5-t9wal/1

- **Version**: 1  
- **Project**: yolo11-iv6di  
- **Dataset Name**: 5-t9wal  
- **Format**: YOLOv8 / YOLOv11 compatible (images + .txt labels)  


Download instructions:  
1. Visit the link and sign up/log in to a free Roboflow account.  
2. Click “Download Dataset” → Select “YOLOv11” or “YOLOv8” format (both are fully compatible).  
3. Unzip the downloaded file to get `train/`, `valid/`, `test/` folders and `data.yaml`.

**Programmatic Download (Recommended)**:
```python
from roboflow import Roboflow
rf = Roboflow(api_key="YOUR_API_KEY")  # Get your free API key at: https://app.roboflow.com/settings/api
project = rf.workspace("yolo11-iv6di").project("5-t9wal")
dataset = project.version(1).download("yolov11")  # Downloads to current directory


