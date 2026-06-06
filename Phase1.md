# Phase 1 — Basic Detection

> *Protecting workers. One frame at a time.*

## 🎯 Goal
Build a script that opens a video file, detects workers frame by frame, checks if they are wearing safety gear, and highlights violations visually on screen.

No alerts. No database. Pure visual detection.

---

## 🧠 What You'll Learn

### Python Fundamentals
- Variables, data types, functions
- Loops and conditionals
- Classes and objects (OOP basics)
- Importing libraries
- File I/O — reading and writing files

### OpenCV
- Reading images and video files
- Understanding frames (a video = thousands of images played fast)
- Drawing rectangles and text on frames
- Displaying video in a window
- Basic image manipulation — resize, color conversion

### YOLOv8 Basics
- What object detection is and how YOLO works
- Loading a pretrained model
- Running inference on a frame
- Reading bounding box coordinates
- Understanding confidence scores

### Putting It Together
- Processing a video frame by frame
- Running YOLO on each frame
- Checking if detected objects include helmet and vest
- Highlighting violations visually on screen

---

## 📁 File Structure

```
vigilance-ai/
├── README.md
├── .gitignore
├── requirements.txt
├── Phase1.md                     ← you are here
├── data/
│   └── test_video.mp4            ← sample factory video for testing
└── src/
    ├── detect.py                 ← main detection script
    └── utils.py                  ← helper functions
```

---

## 📄 What Each File Does

### `src/detect.py`
The main script you run. It will:
1. Open `data/test_video.mp4`
2. Loop through every frame
3. Run YOLOv8 on each frame
4. Check if helmet or vest is missing
5. Draw a red bounding box around the violation
6. Display it on screen in real time

### `src/utils.py`
Small reusable helper functions:
- `draw_label()` — draws text on a frame neatly
- `is_violation()` — checks if PPE is missing from detections
- `save_snapshot()` — saves a frame as a `.jpg` image

### `data/`
Holds the test video used during development.
Download a sample factory/construction worker video from YouTube using `yt-dlp` and place it here as `test_video.mp4`.

---

## 📦 Requirements

```
opencv-python
ultralytics
numpy
```

Install with:
```bash
pip install -r requirements.txt
```

---

## 🗓️ Weekly Plan

| Week | Focus |
|------|-------|
| Week 1 | Python fundamentals — functions, loops, OOP, file I/O |
| Week 2 | OpenCV basics — images, video, drawing, frames |
| Week 3 | YOLOv8 — load model, run inference, read detections |
| Week 4 | Connect everything — working Phase 1 demo |

---

## ✅ Phase 1 Checklist

- [ ] Set up project folder structure
- [ ] Write `requirements.txt`
- [ ] Learn Python basics (Week 1)
- [ ] Learn OpenCV basics (Week 2)
- [ ] Load YOLOv8 and run on an image (Week 3)
- [ ] Process test video frame by frame (Week 3)
- [ ] Draw bounding boxes on violations (Week 4)
- [ ] Working demo — video plays with violation highlights (Week 4)

---

## 🔜 What Comes After Phase 1

Once this works, Phase 2 adds:
- Audio alarm on violation
- Screenshot saved automatically
- SMS alert to factory manager via Twilio

See the full roadmap in `Vigilance_AI_Roadmap.pdf`.
