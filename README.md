
# YOLO-Based Object Detection on Resized KITTI Images

This project implements a YOLO-style object detection model trained on KITTI-resolution images that were resized to suit smaller YOLO architectures. It follows a YOLOv1-like, anchor-free approach using a Darknet-53 backbone with transfer learning. Future improvements include integrating anchors for better bounding box quality.

## Overview

The original dataset consists of images with a resolution of **1242×375**, which is large for compact YOLO models. To make training feasible while preserving the aspect ratio, images were resized to **640×192**.

A YOLOv1-style grid-based detection head is used without predefined anchors. The backbone is **Darknet-53**, initialized with pretrained weights for faster convergence.

## Key Features

* **Aspect-ratio–preserving image preprocessing**
  Images resized from 1242×375 to 640×192.

* **YOLOv1-style, anchor-free detection head**
  Grid-based classification and bounding box regression.

* **Darknet-53 backbone with transfer learning**
  Stabilizes early training and improves convergence.

* **Accurate confidence predictions**
  The model produces reliable confidence scores on test samples.

* **Planned anchor support**
  Future iterations will integrate anchors to improve detection quality.

## Workflow

1. **Data Preprocessing**

   * Resize images to 640×192.
   * Convert labels to YOLOv1-compatible grid format.

2. **Model Architecture**

   * Darknet-53 backbone (pretrained).
   * Anchor-free YOLOv1-style detection head.

3. **Training Setup**

   * Transfer learning enabled.
   * YOLO-style composite loss (classification, confidence, localization).

4. **Evaluation**

   * Stable confidence predictions.
   * Reasonable bounding box performance for an anchor-free model.

## Resuts
![alt text](path/to/image.png)
![alt text](path/to/image.png)
## Future Work

* Add anchor-based predictions.
* Experiment with multi-scale training.
* Evaluate with metrics like mAP.
* Explore YOLOv3-style heads once anchors are integrated.

## Tech Stack

* Python
* PyTorch
* Darknet-53 pretrained weights
* KITTI (or similar) dataset

## How to Run

```bash
git clone <your-repo-url>
cd <repo>
```
### Train the model

```bash
yolov1/yolov1.ipynb
```




