# FAO-Sofiya-Tumanova

This repository contains code, models, and resources developed during work with the **Food and Agriculture Organization of the United Nations (FAO)** to support vessel detection using drone and satellite imagery. The goal of this work is to improve monitoring of small artisanal fishing vessels by applying computer vision techniques to high-resolution earth observation data.

---

## Repository Structure

The repository is organized into three main folders:

- **`Vessel_Detection_Drone_Imagery/`**
  - Contains code for detecting vessels from **Drone-based orthomosaic imagery**.
  - Includes links to Caribbean vessel annotations and pretrained YOLOv8 model weights (`best.pt`) that can be used for training, fine-tuning, or testing.

- **`Vessel_Detection_Pleiades_Imagery/`**
  - Contains code for detecting vessels from **Pleiades very high-resolution satellite imagery**.

- **`Vessel_Detection_Satellite_Imagery/`**
  - Contains code for processing **Google Maps very high resolution imagery** for vessel detection and related applications.
  - Includes links to Caribbean vessel annotations and pretrained YOLOv8m-obb model weights (`best.pt`) that can be used for training, fine-tuning, or testing.

Each sub-folder contains a `code/` directory with Python scripts for model training, inference, and data processing.

---

## Features

- Vessel detection from **Drone, Pleiades, and Google Maps imagery**.
- Annotated datasets from the **Caribbean region** (links provided in relevant folders).
- Pretrained YOLO model weights (`best.pt`) available for download to:
  - Train from scratch.
  - Fine-tune on new datasets.
  - Run inference and evaluate performance.

---

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/<your-username>/FAO-Sofiya-Tumanova.git
   cd FAO-Sofiya-Tumanova
   ```
2. Navigate to the desired folder:

**`Vessel_Detection_Drone_Imagery/`**

**`Vessel_Detection_Pleiades_Imagery/`**

**`Vessel_Detection_Satellite_Imagery/`**

3. Follow instructions in the respective `code/` folder to run detection scripts.

4. Download the **annotations** and **pretrained model weights** `(best.pt)` from the links provided inside each folder to train, fine-tune, or test the models.

---
## Requirements

Python 3.8+
PyTorch
YOLO dependencies from Ultralytics
GDAL, Rasterio, and other geospatial libraries (for preprocessing satellite data)

---
## Acknowledgements

This repository was developed by **Sofiya Tumanova** in collaboration with the **FAO Fisheries and Aquaculture Division (NFI)** as part of efforts to strengthen monitoring of small-scale fisheries and vessel activity using remote sensing, GIS, and AI tools.
