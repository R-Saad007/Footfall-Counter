# Pytorch-YOLO Footfall Counter
Implemented logic to count footfall for a given video clip.

## Simple Logic:
- Check for track ID of an object and increment whenever the object crosses the designated area (green area) **FROM ABOVE** (Ensure only movement towards the area from top to bottom is considered)
- Making use of 2 dictionaries to store the state of the tracked objects (inside)

## Cases Handled:
- People entering
- People exiting
- People re-entering (same individual have similar track_id)

## Need to clone ByteTrack and Yolov5 repositories
### ByteTrack
```git clone https://github.com/ifzhang/ByteTrack.git```

```pip install -r requirements.txt```

```python3 setup.py develop```

```pip install cython_bbox```
### YOLOv5
```git clone https://github.com/ultralytics/yolov5.git```

```pip install -r requirements.txt```
## Directory structure:
### ByteTrack -> YoloV5 + handler.py + video_folder(videos)
### Script Execution
```python handler.py -vid_path (video path from script's directory)```
### A JSON file with the coordinates for each bounding box is also created
