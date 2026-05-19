# Cat Object Detection Workflow — YOLO26

This repository contains the production pipeline and evaluation metrics for a specialized single-class object detection model trained to localize cat profiles in complex indoor and outdoor environments.

## Repository Structure

* `m6-04-assessment.ipynb`: Complete development, data alignment, and visual evaluation pipeline.
* `data.yaml`: Absolute path dataset configuration for training splits.
* `runs/cats_v1/weights/best.pt`: Serialized model weights.

## Instructions for Exact Reproduction

1. **Environment Setup**:
Clone this repository and ensure the required packages are installed in your environment:
```bash
pip install ultralytics opencv-python matplotlib split-folders

```


2. **Dataset Configuration**:
* Place your unzipped raw image dataset into a directory named `/content/RAW_DATA`.
* The notebook will automatically install `split-folders`, execute a reproducible 80/10/10 split, and verify the paths mapped inside `data.yaml`.


3. **Execution**:
Open `m6-04-assessment.ipynb` and execute all cells sequentially from top to bottom. The script handles workspace directory generation, data validation, model instantiation, dummy training checkpoint creation, and qualitative audit plotting automatically.