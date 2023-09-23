# setup

```
conda create -n yolov8_custom python=3.9
conda activate yolov8_custom
pip install ultralytics
pip install --upgrade torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
```

# tart training

```
yolo task=detect mode=train model=yolov8m.pt data=data_custom.yaml epochs=30 imgsz=640 batch=8
```

# use model

```
yolo task=detect mode=predict model=runs/detect/train/weights/best.pt show=True conf=0.3 source=1.jpg
```

# clearing up

- delete `runs` folder
- delete `yolov8m.pt` file
- delete `yolov8n.pt` file
- delete `train/labels.cache` file
- delete `val/labels.cache` file

# version info

- conda 23.7.2
- ultralytics 8.0.184
- pip 23.2.1
- python 3.9
- cuda 11.7
- pytorch 2.0.1
