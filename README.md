# setup

```
conda create -n yolov8_custom python=3.9
conda activate yolov8_custom
pip install ultralytics
pip install --upgrade torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
```

# tart training

```
yolo task=detect mode=train model=yolov8s.pt data=data_custom.yaml epochs=20 imgsz=640 batch=6
```

# use model

```
yolo task=detect mode=predict model=runs/detect/train/weights/best.pt show=True conf=0.5 source=1.jpg
```
