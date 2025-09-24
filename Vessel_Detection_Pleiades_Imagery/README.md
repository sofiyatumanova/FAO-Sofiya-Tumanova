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
# Pleiades Imagery – Detection Results

Below are sample outputs from the vessel detection model applied to **Pleiades satellite imagery** at 0.5m/pixel resolution.

---

![Result 1](RESULTS_Imagery/download%20(1).png)
![Result 2](RESULTS_Imagery/download%20(13).png)
![Result 3](RESULTS_Imagery/download%20(15).png)
![Result 4](RESULTS_Imagery/download%20(4).png)
