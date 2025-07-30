#  YOLOv5 Custom Object Detection Model

This repository contains a YOLOv5 model trained on a custom dataset with optimized accuracy through evolutionary hyperparameter tuning. Ideal for applications in robotics, smart systems, or real-world object detection.

##  Overview
- **Architecture**: YOLOv5
- **Training Image Size**: 640 × 640
- **Batch Size**: 16
- **Epochs**: 100
- **Optimization Method**: Evolution (`--evolve`)
- **Exported Formats**: `.pt` for PyTorch, `.onnx` for deployment

##  Training Features
- Auto-tuned hyperparameters using YOLO's genetic evolution
- Advanced augmentations (Mosaic, HSV, Flip)
- Anchor box refinement for better bounding box localization

##  Model Performance
| Metric       | Score     |
|--------------|-----------|
| mAP@0.5      | 89.67 %   |
| Precision    | 95.20 %   |
| Recall       | 84.36 %   |
| F1-Score     | 89.67 %   |

> Replace the scores above after evaluating your model using `results.csv` or TensorBoard in `runs/evolve/`

##  Files Included
- `best.pt` – Final trained weights
- `data.yaml` – Dataset configuration
- `README.md` – Documentation and usage instructions

##  Inference Example
Run detection on test images:
```bash
python detect.py --weights best.pt --source test_images/
