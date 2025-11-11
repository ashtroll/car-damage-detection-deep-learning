# Download Pre-trained Model Weights

Due to GitHub file size limitations, trained model weights are not included in this repository.

## Option 1: Download Pre-trained Weights (Recommended)

If pre-trained weights are available, download them from:
- [Releases page](https://github.com/Oleksy1121/Car-damage-detection/releases)
- Google Drive / Dropbox link (if provided)

Place the `best.pt` file in: `damage_detection_app/model/best.pt`

## Option 2: Train Your Own Model

Follow the training instructions in the [README](README.md#4-model-training--evaluation) or [QUICKSTART](QUICKSTART.md#training-your-own-model) guide.

### Quick Training Steps:
```bash
# 1. Prepare your dataset (Roboflow YOLOv8 format)
# 2. Activate environment
conda activate car-damage

# 3. Train model
yolo task=detect mode=train model=yolov8s.pt data=path/to/data.yaml epochs=100 imgsz=640 batch=16

# 4. Copy trained weights
cp runs/detect/train/weights/best.pt damage_detection_app/model/best.pt
```

## Model Specifications

The default trained model has:
- **Architecture**: YOLOv8s (small)
- **Input size**: 640x640
- **Classes**: scratches, dents, rust, paint defects, etc.
- **mAP50**: ~0.48 (on validation set)
- **File size**: ~22MB

## Using Custom Models

You can use any YOLOv8-compatible model:
1. Place your `.pt` file in `damage_detection_app/model/`
2. Ensure class names match your training dataset
3. The app will automatically load and use it

## Need Help?

Open an [issue](https://github.com/Oleksy1121/Car-damage-detection/issues) if you need assistance obtaining or training a model.
