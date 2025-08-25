# Object Detection of Gloved Hands vs Bare Hands using YOLOv5

This repository demonstrates **object detection using YOLOv5** to classify and locate **gloved hands** and **bare hands** in images. The project uses a **custom dataset** of hand images and includes scripts for training, validation, inference, visualization, and saving results in multiple formats.

---

## Features

- Train YOLOv5 on a custom **gloved vs bare hand dataset**.
- Perform **validation** and visualize results:
  - Training & validation loss curves
  - Confusion matrix
  - Precision, Recall, and PR/F1 curves
- Run **inference on test images** and visualize predictions.
- Save **detection results** as images, text files, and **JSON files** for further analysis.
- Export training, validation, and detection outputs for easy reuse.

---

## Dataset
Download the file in YOLOv5 format from: (Roboflow)[<https://universe.roboflow.com/glove-uylxg/glove-q7czq/dataset/1>] and upload it in your drive.
The dataset contains labeled images of hands, categorized as:

- `gloved_hand`
- `bare_hand`

It is organized into **train**, **validation**, and **test** sets. 

---

## Workflow

1. **Setup Environment**
   - Mount Google Drive (if using Colab)
   - Install dependencies
   - Clone YOLOv5 repository

2. **Prepare Dataset**
   - Unzip dataset
   - Create dataset YAML configuration

3. **Training**
   - Train YOLOv5 on the dataset
   - Training outputs are saved in `/runs/train/exp`

4. **Validation**
   - Evaluate model on validation set
   - Outputs include:
     - Confusion matrix
     - Precision-Recall curves
     - F1-score curves

5. **Inference / Detection**
   - Run detection on test images
   - Predicted images and labels are saved in `/runs/detect/exp`
   - Detection labels converted to JSON for further analysis

6. **Visualization**
   - Visualize:
     - Training and validation loss curves
     - Confusion matrix
     - PR/F1 curves
     - Sample predictions with bounding boxes

7. **Saving & Exporting Results**
   - Save training, validation, and detection outputs as ZIP files
   - Copy results to Google Drive for backup or further use

---

## Outputs

- **Training Results:** `/runs/train/exp`  
  - Weights (`best.pt`), `results.png`, `results.csv`
- **Validation Results:** `/runs/val/exp`  
  - Confusion matrix, PR curves, F1 curves
- **Detection Results:** `/runs/detect/exp`  
  - Predicted images, text labels, JSON files for detections

---

## Notes

- Paths in the workflow should be updated if files are moved or directories are changed.
- The pipeline is designed for **Google Colab**, but it can be adapted for local environments.
- This project provides a **complete end-to-end YOLOv5 pipeline**: training → validation → detection → saving results → visualization.
