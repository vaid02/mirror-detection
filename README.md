# mirror-detection

---

## 📦 Features

- ✅ Custom mirror detection with YOLOv8
- ✅ ONNX export support for cross-platform deployment
- ✅ Real-time video and image inference
- ✅ Supports CPU and GPU acceleration
- ✅ Easy dataset setup with YOLO-compatible structure

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
train: images                     # Folder with training images
val: val/images                   # Folder with validation images

nc: 1                             # Number of classes
names: ['mirror']                 # Class name

