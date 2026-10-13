# Applied Computer Vision with YOLO: Object Detection and Instance Segmentation

Workshop materials and reference resources

---

## Abstract

This repository contains the materials for a hands-on workshop on applied computer vision using the YOLO (You Only Look Once) family of models. The session introduces the foundations of computer vision, explains the architecture and historical development of YOLO, and demonstrates a complete workflow for building a custom dataset, annotating it, and training a model for two tasks: object detection and instance segmentation.

## Workshop Details

| Field | Detail |
|---|---|
| Title | Applied Computer Vision with YOLO: Detection and Segmentation |
| Trainer | Muhammad Fiaz |
| Co-trainer | Muhammad Haris Khan |
| Moderators | Mahrukh Haseeb, Saad Umar |
| Format | Online, instructor-led, hands-on |
| Date | [DD Month YYYY] |
| Organizer | [Organization name] |

## Learning Objectives

After completing this workshop, participants should be able to:

1. Describe the core concepts of computer vision and its practical applications.
2. Explain the architecture of YOLO and trace its evolution across versions.
3. Distinguish between object detection and instance segmentation.
4. Build and annotate a custom image dataset suitable for training.
5. Train a YOLO model on custom data for detection and segmentation tasks.
6. Run inference with the trained model on unseen images.

## Workshop Outline

| Part | Topic | Description |
|---|---|---|
| 1 | Introduction to Computer Vision | Overview of the field, key tasks, and real-world impact |
| 2 | YOLO Architecture and Evolution | Design principles of single-stage detection and the development of the YOLO family |
| 3 | Custom Dataset Creation and Annotation | Data collection, labeling for bounding boxes and segmentation masks, dataset formatting |
| 4 | Model Training | Training YOLO on custom data for object detection and instance segmentation |

## Resources

| Resource | Link |
|---|---|
| Session recording | https://youtu.be/sWxLWTyNsS8 |
| Presentation slides | https://canva.link/tsaosm4hh81p4zv |
| Colab notebook 1 | https://colab.research.google.com/drive/1HetgQwTLgM15zm2hjC9lAXS3wgjQYhKM?usp=sharing |
| Colab notebook 2 | https://colab.research.google.com/drive/1ElY_MevQuaC3-k84KsdO_gME4sR_NOjB?usp=sharing |

## Prerequisites

- Basic proficiency in Python
- Familiarity with fundamental machine learning concepts
- A Google account for accessing Google Colab (no local installation required)

## Reproducing the Workflow

1. Review the session recording and slides to understand the conceptual background.
2. Open each Colab notebook and create a personal copy (File, then Save a copy in Drive).
3. Enable GPU acceleration (Runtime, then Change runtime type, then select a GPU).
4. Execute the notebooks sequentially.
5. Substitute your own annotated dataset to train a custom model.

### Minimal Example (Ultralytics API)

The following snippet illustrates the general training and inference procedure. Model weights and hyperparameters should be adjusted to the task and dataset.

```bash
pip install ultralytics
```

```python
from ultralytics import YOLO

# Object detection
model = YOLO("yolov8n.pt")

# Instance segmentation (alternative)
# model = YOLO("yolov8n-seg.pt")

# Train on a custom dataset described by data.yaml
model.train(data="data.yaml", epochs=50, imgsz=640)

# Evaluate on the validation split
metrics = model.val()

# Run inference on a new image
results = model.predict("image.jpg", save=True)
```

## Repository Structure

```
.
├── README.md
└── (add notebooks, slides export, or sample data here if desired)
```

## References

1. Redmon, J., Divvala, S., Girshick, R., and Farhadi, A. (2016). You Only Look Once: Unified, Real-Time Object Detection. Proceedings of the IEEE Conference on Computer Vision and Pattern Recognition (CVPR). https://arxiv.org/abs/1506.02640
2. Ultralytics. YOLO Documentation. https://docs.ultralytics.com

## Acknowledgments

The trainer thanks the co-trainer, the moderators, and all participants for their contributions to the session.

## Author

Muhammad Fiaz
Bachelor of Information Technology, University of Sargodha
