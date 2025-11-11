# Quick Start Guide 🚀

This guide will help you get the Car Damage Detection system up and running in minutes.

## Prerequisites
- Python 3.10 or higher (3.12 recommended)
- NVIDIA GPU with CUDA support (optional, for training)
- 8GB RAM minimum (16GB recommended for training)

## Installation

### Option 1: Quick Setup (Recommended)

1. **Clone the repository**
   ```bash
   git clone https://github.com/Oleksy1121/Car-damage-detection.git
   cd Car-damage-detection
   ```

2. **Create virtual environment**
   ```bash
   # Using conda (recommended)
   conda create -n car-damage python=3.12
   conda activate car-damage
   
   # OR using venv
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Download pre-trained weights** (if available)
   - Place `best.pt` in `damage_detection_app/model/`
   - Or train your own model (see Training section below)

5. **Run the GUI**
   ```bash
   cd damage_detection_app
   python app.py
   ```

## Using the Application

1. **Launch** the app using the command above
2. **Load images** by:
   - Clicking "Open Folder" and selecting a directory with car images
   - Or drag-and-drop a folder into the window
3. **Navigate** through images using Previous/Next buttons
4. **View detections** in the log panel on the right

## Training Your Own Model

1. **Prepare dataset** (Roboflow export in YOLOv8 format)
2. **Open training notebook**: `training/YOLOv8.ipynb`
3. **Update data path** in the notebook to point to your `data.yaml`
4. **Run all cells** to start training
5. **Export weights** from `runs/detect/trainX/weights/best.pt` to `damage_detection_app/model/`

### Quick Training via CLI
```bash
conda activate car-damage
yolo task=detect mode=train model=yolov8s.pt data=path/to/data.yaml epochs=100 imgsz=640 batch=16
```

## Common Issues

**Import Error: No module named 'cv2'**
- Solution: `pip install opencv-python`

**Model file not found**
- Ensure `best.pt` is in `damage_detection_app/model/`
- Check file permissions

**CUDA out of memory**
- Reduce batch size: `batch=8` or `batch=4`
- Use smaller model: `yolov8n.pt` or `yolov8s.pt`

## Next Steps
- Read the full [README](README.md) for detailed architecture
- Check [CONTRIBUTING.md](CONTRIBUTING.md) to contribute
- Explore training notebooks in `training/`

## Support
- 📫 Open an [issue](https://github.com/Oleksy1121/Car-damage-detection/issues)
- 💬 Start a [discussion](https://github.com/Oleksy1121/Car-damage-detection/discussions)
