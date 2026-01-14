# YOLO-CSB: Enhanced Apple Detection and 3D Localization in Occluded Orchard Environments

This repository contains the official implementation of **YOLO-CSB**, an improved lightweight object detection model based on YOLO11s, specifically designed for accurate apple detection and 3D localization in complex orchard scenes with heavy leaf and fruit occlusion.

YOLO-CSB incorporates the following key enhancements:
- **CSFC Block** (lightweight backbone reconstruction) for reduced model size and improved efficiency
- **SEAM** (occlusion-aware feature restoration module) to better handle occluded regions
- **BiFPN** (efficient bidirectional feature pyramid network) for enhanced multi-scale feature fusion and higher detection precision

Combined with an RGB-D camera, the model enables precise 3D positioning of detected apples, supporting robotic harvesting applications.

## Abstract (from the paper)

Apples are cultivated over a large global area with high yields, and efficient robotic harvesting requires accurate detection and localization, particularly in complex orchard environments where occlusion by leaves and fruits poses substantial challenges. To address this, we proposed a YOLO-CSB model-based method for apple detection and localization, designed to overcome occlusion and enhance the efficiency and accuracy of mechanized harvesting. Firstly, a comprehensive apple dataset was constructed, encompassing various lighting conditions and leaf obstructions, to train the model. Subsequently, the YOLO-CSB model, built upon YOLO11s, was developed with improvements including the integration of a lightweight CSFC Block to reconstruct the backbone, making the model more lightweight; the SEAM component is introduced to improve feature restoration in areas with occlusions, complemented by the efficient BiFPN approach to boost detection precision. Additionally, a 3D positioning technique integrating YOLO-CSB with an RGB-D camera is presented. Validation was conducted via ablation analyses, comparative tests, and 3D localization accuracy assessments in controlled laboratory and structured orchard settings. The YOLO-CSB model demonstrated effectiveness in apple target recognition and localization, with notable advantages under leaf and fruit occlusion conditions. Compared to the baseline YOLO11s model, YOLO-CSB improved mAP by 3.02% and reduced the parameter count by 3.19%. Against mainstream object detection models, YOLO-CSB exhibited significant advantages in detection accuracy and model size, achieving an mAP of 93.69%, precision of 88.82%, recall of 87.58%, and a parameter count of only 9.11 M. The detection accuracy in laboratory settings reached 100%, with average localization errors of 4.15 mm, 3.96 mm, and 4.02 mm in the X, Y, and Z directions, respectively. This method effectively addresses complex occlusion environments, enabling efficient detection and precise localization of apples, providing reliable technical support for mechanized harvesting.

## Key Performance Metrics (YOLO-CSB)

- mAP@50: **93.69%**  
- Precision: **88.82%**  
- Recall: **87.58%**  
- Parameters: **9.11 M**  
- Improvement over YOLO11s: +3.02% mAP, -3.19% parameters  
- 3D Localization Errors (lab): X: 4.15 mm, Y: 3.96 mm, Z: 4.02 mm  
- Detection Accuracy in Lab: **100%**

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/[your-username]/YOLO-CSB.git
Dataset Link: https://app.roboflow.com/yolo11-i6di/5-t9wal/1
**Programmatic Download (Recommended)**:
```python
from roboflow import Roboflow
rf = Roboflow(api_key="YOUR_API_KEY")  # Get your free API key at: https://app.roboflow.com/settings/api
project = rf.workspace("yolo11-iv6di").project("5-t9wal")
dataset = project.version(1).download("yolov11")  # Downloads to current directory


