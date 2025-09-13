# Caribbean Vessel Detection - Drone Imagery (YOLOv8m Custom Model)

## Project Overview
This repository contains resources for detecting vessels in **drone orthomosaic imagery** using a custom **YOLOv8m model**. The work supports FAO initiatives such as vessel monitoring, national vessel registry updates, and maritime research.  

The repository is organized into folders for **code**, **model weights**, and **annotations**, with large files hosted externally on Dropbox.

---

## Folder Structure on GitHub

- **code/** → Scripts for:
  - Tiling large orthomosaic drone images into smaller patches, and resampling to 10cm/pixel if needed. Running inference on tiled images using the trained model.
  - Fine-tuning the model with new vessel annotations (Iterative Dataset Improvement).  
- **best_model_weights/** → Placeholder text file with link to trained model weights.  
- **annotations/** → Placeholder text file with link to training/validation/test annotations (RoboFlow export).    
- **README.md** → Documentation for the repository.  

> ⚠️ Large files are stored on Dropbox for easy access and to keep this repository lightweight.

---

## Large Files (Dropbox)

### 1. Model Weights
**File:** `2nd-fine-tuning-yolov8m-best.pt`  
**Description:** Trained YOLOv8m model for vessel detection in drone imagery. Use this file to run inference or fine-tune the model.  

**Download link:** [(https://www.dropbox.com/scl/fi/pr8ktsz0ugj9kga6aeqf6/2nd-fine-tuning-yolov8m-best.pt?rlkey=5beu2iled7vbbvejusq4v6s09&st=ia7ape09&dl=0)]

---

### 2. Vessel Annotations
**File:** `CLEAN Vessel from Drone Imagery.v3i.yolov8`  
**Description:** RoboFlow export containing the annotated dataset split into **train, validation, and test sets**. Includes all labeled vessel objects needed for training.  

**Download link:** \[(https://www.dropbox.com/scl/fi/i83hj73a71uqk1mmpf45c/CLEAN-Vessel-from-Drone-Imagery.v3i.yolov8.zip?rlkey=2bzph84yoahmi7pry3g4izsfr&st=p2ne8kpz&dl=0)]

---

## Usage

### Inference with Ultralytics YOLOv8

You can use this model like any other YOLOv8 model from Ultralytics:

```python
from ultralytics import YOLO

# Load your fine-tuned model
model = YOLO("path_to_best.pt")

# Run prediction on a single image
results = model.predict("example_image.jpg", imgsz=1024, conf=0.25)

# Print results
results.print()

# Save predictions to disk
results.save()
```

## Training 
Use the **File:** `CLEAN Vessel from Drone Imagery.v3i.yolov8` and **File:** `data.yaml` to train or fine-tune the model.
Training scripts are located in the code/ folder.

### Example data.yaml format (for reference):
```yaml
train: train/images
val: valid/images
test: test/images

names: 
  0: catamaran
  1: fishing-vessels
  2: other-vessels
  3: private-yachts
  4: recreational-boat
```
---
## Notes
Ensure all large files are downloaded from Dropbox links before running inference or training.

GitHub folders (best_model_weights/, annotations/) contain placeholder instructions with external links.

---
## Citation 
If using this model or dataset in your research, please cite:

Sofiya Tumanova, 2025

For the base YOLOv8 model, please also acknowledge Ultralytics:
Ultralytics YOLOv8
[https://github.com/ultralytics/ultralytics], Glenn Jocher et al.
