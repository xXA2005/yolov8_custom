# setup

```
conda create -n yolov8_custom python=3.9
conda activate yolov8_custom
pip install ultralytics
pip install --upgrade torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu117
```

# start training

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
