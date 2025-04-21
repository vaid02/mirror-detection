# mirror-detection

---

## 📦 Features

- ✅ Custom mirror detection with YOLOv8
- ✅ ONNX export support for cross-platform deployment
- ✅ Real-time video and image inference
- ✅ Supports CPU and GPU acceleration
- ✅ Easy dataset setup with YOLO-compatible structure

---

## 🔍 Objective

Mirrors can mislead AI vision systems—particularly in robotics or drone navigation—by presenting reflections as real objects or paths. This model helps to **detect and identify mirrors in real-time video streams or images**, enabling smarter, safer decision-making.

---

## 📁 Dataset - MSD

This project uses a custom dataset called **MSD** (Mirror Surface Dataset).

### Dataset Format

- **YOLOv8 Format**
  - Each image has a corresponding `.txt` file with labels in YOLO format.
  - Label format:  
    `class_id center_x center_y width height` (all normalized values)

### Data Configuration (`data.yaml`)

```yaml
path: MSD/training                # Root directory for training data
train: MSD/train/images                    # Folder with training images
test: MSD/test/images                  # Folder with validation images

nc: 1                             # Number of classes
names: ['mirror']                 # Class name
```
📦 Download dataset: [Google Drive link](https://drive.google.com/drive/folders/1uIwLq1fSGvAVQhgAzU1Q7tI2ZmRPj1Rg?usp=drive_link)
### Dataset Directory
```yaml
MSD/
└── train/
    └── images/
    └── labels/
└── test/
    └── images/
    └── labels/
```
### Applications
1. Drone Navigation in Indoor Environments

Drones using computer vision can misinterpret reflections in mirrors as real obstacles or paths. Detecting mirrors helps prevent crashes and incorrect navigation, making this solution a cost-efficient alternative to expensive LIDAR systems in some indoor use-cases.

2. Autonomous Vehicle Safety

Mirrors or reflective surfaces in parking lots or roadsides can mislead vehicle detection systems. Detecting mirrors enhances safety and decision-making for autonomous driving systems.

3. Smart Surveillance & Security Systems

Surveillance cameras can misinterpret mirror reflections as intrusions or additional people. Detecting mirrors enables accurate headcount, activity monitoring, and intrusion detection in high-security zones.
