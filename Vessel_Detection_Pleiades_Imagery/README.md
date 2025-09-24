# Caribbean Vessel Detection on Pleiades 0.5m/pixel Satellite Imagery (YOLOv8m-OBB Custom Model)

## Project Overview
This repository contains resources for detecting vessels in **Pleiades high-resolution satellite imagery** using a custom **YOLOv8m-OBB model**. The work supports FAO initiatives such as vessel monitoring, national vessel registry updates, and maritime research.  

The repository contains:

- **Code** for running inference on Pleiades imagery using the trained model.
- Folder structure to organize results, scripts, and placeholders for model weights.
- Links to large files hosted externally on Dropbox.

> ⚠️ Large files (model weights) are hosted on Dropbox for easy access and to keep this repository lightweight.

---

## Folder Structure on GitHub

- **code/** → Contains scripts for inference and model testing:
  - `testing_model_on_pleiades.py` → Python script to run vessel detection using the YOLOv8m-OBB model on Pleiades imagery.  
  - `Testing_model_on_Pleiades.ipynb` → Jupyter Notebook for interactive testing and visualization of results.  
- **README.md** → Documentation for the repository.  

> Before running any code, you must download the trained YOLOv8m-OBB model weights (`best.pt`) from the [Vessel_Detection_Satellite_Imagery README.md Dropbox link](https://www.dropbox.com/scl/fi/lh385t61iee52r4d3hyo0/best.pt?rlkey=7gsyw8qo3dpkxc2uueyf8ba6e&st=z9fufaa6&dl=0)
.

---
## Pleiades Imagery – Detection Results

Below are sample outputs from the vessel detection model applied to **Pleiades satellite imagery** at 0.5m/pixel resolution.

---

![Result 1](RESULTS_Imagery/download%20(1).png)
![Result 2](RESULTS_Imagery/download%20(13).png)
![Result 3](RESULTS_Imagery/download%20(15).png)
![Result 4](RESULTS_Imagery/download%20(4).png)

---
## Code Summary
The Colab notebook provides an **end-to-end detection pipeline**:  
- Installing dependencies (`ultralytics`, `opencv`, `rasterio`).  
- Loading and converting **16-bit Pleiades imagery** to 8-bit RGB for model input.  
- Rescaling imagery from 0.5 m/pixel to match the training resolution (0.3 m/pixel).  
- **Tiling large images** into 640×640 patches with overlap to avoid edge losses.  
- Running YOLOv8m-OBB vessel detection on all tiles.  
- **Reprojecting predictions into georeferenced coordinates** and exporting as GeoJSON.  
- Saving annotated tiles, bounding box labels, and detection results to Google Drive.  
- Optionally zipping and downloading the results.  
- Comparing **Pleiades tiles (0.5 m/pixel)** with **Google Maps tiles (0.3 m/pixel)** side by side for quality assessment.  

This workflow ensures geospatial accuracy and allows large-scale vessel detection from satellite imagery.  

---
## Notes

Ensure you download the `best.pt` model weights before running any code.

The code was developed specifically for detecting Caribbean vessels in Pleiades high-resolution imagery.

Adjust the imgsz, conf, and file paths according to your local setup.

---
## Citation

If using this model or dataset in your research, please cite:

Sofiya Tumanova, 2025

For the base YOLOv8 model, please also acknowledge Ultralytics:
Ultralytics YOLOv8, Glenn Jocher et al., https://github.com/ultralytics/ultralytics
