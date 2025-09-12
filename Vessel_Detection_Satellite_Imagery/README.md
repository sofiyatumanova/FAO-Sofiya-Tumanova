# Caribbean Vessel Detection - YOLOv8m-OBB Custom Model

## Project Overview
This repository contains resources for detecting vessels in the Caribbean region using a custom **YOLOv8m-OBB model**. The goal is to support FAO initiatives such as vessel monitoring, infrastructure mapping, and maritime research.  

The repository contains:

- **Code** for training, inference, and evaluation of the model.
- Folder structure to organize results, models, and scripts.
- Links to large files hosted externally on Dropbox.

---

## Folder Structure on GitHub


> Large files are stored on Dropbox for easy access and to keep this repository lightweight.

---

## Large Files (Dropbox)

### 1. Model Weights
**File:** `best.pt`  
**Description:** Trained YOLOv8m-OBB model for vessel detection. Use this file to run inference or fine-tune the model.

**Download link:** [Insert Dropbox link here]

---

### 2. Vessel Annotations
**File:** `Vessel Object Detection.v9i.yolov8-obb`  
**Description:** RoboFlow export containing the annotated dataset split into **train, validation, and test sets**. Includes all labeled vessel objects needed for training.

**Download link:** [Insert Dropbox link here]

---

### 3. Test Metrics and Predictions
**File:** `test-metrics-yolov8m-obb.zip`  
**Description:** Contains evaluation outputs automatically generated during `model.predict` on the test set:  
- Confusion matrices  
- Batch prediction images  
- Performance graphs  

**Download link:** [Insert Dropbox link here]


