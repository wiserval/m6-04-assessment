# Cat Object Detection Workflow — YOLO26

This repository contains the production pipeline and evaluation metrics for a specialized single-class object detection model trained to localize cat profiles in complex indoor and outdoor environments.

## Repository Structure

* `m6-04-assessment.ipynb`: Complete development, data alignment, and visual evaluation pipeline.
* `data.yaml`: Dataset configuration file pointing to training splits.
* `runs/cats_v1/weights/best.pt`: Serialized model weights.
* `.gitignore`: To keep repository clean and ensure only the necessary weights are pushed.

## Instructions for Exact Reproduction

1. **Environment Setup**:
Clone this repository and ensure the required packages are installed in your environment:
```bash
pip install ultralytics opencv-python matplotlib pyyaml gdown

```


2. **Dataset Configuration**:
* The notebook handles dataset acquisition automatically via `gdown`. It pulls the 3,327 verified image-label pairs directly from the configured Google Drive source.
* Execution will automatically extract the files to `/content/data/DATA_CLEAN/` and perform a reproducible train/val/test split as defined in Task 2.


3. **Execution**:
Open `m6-04-assessment.ipynb` and execute all cells sequentially from top to bottom. The script handles:
* **Workspace Generation**: Creating the necessary `data/` directory structure.
* **Data Validation**: Confirming the integrity of the 3,327 image-label pairs.
* **Model Training**: Utilizing the YOLO26 framework on the A100 GPU instance.
* **Qualitative Audit**: Automatically plotting detections for visual evaluation.