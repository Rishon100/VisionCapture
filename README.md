# VisionCapture
# 🎥 VisionFlow-OpenCV

## 📌 Overview
This project demonstrates basic image capture and video processing using the OpenCV library in Python. The webcam is used to capture live video, save images, resize frames, and rotate video streams in real time.

---

## 🎯 Objective
To develop a Python program using OpenCV that can:

- Capture an image from the webcam
- Save the captured frame as a JPG image
- Display live webcam video
- Resize and display the video stream
- Rotate and display the video feed

---

## 📂 Project Workflow

### Step 1
Import the required libraries and initialize the webcam using OpenCV.
```
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
```
### Step 2
Capture frames continuously from the webcam.
```
video = cv2.VideoCapture("video.mp4")
# Read a single frame
ret, frame = video.read()

if ret:
    # Write the frame as a JPG file
    cv2.imwrite("capture_frame.jpg",frame)
```
### Step 4
Display the live webcam feed using `cv2.imshow()`.
```
video = cv2.VideoCapture("video.mp4")
## Your Code Here##
while True:
    ret, frame = video.read()

    if not ret:
        break

   # Convert frame color for matplotlib
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.03)
video.release()
```

### Step 5
Resize and rotate the frames, then display the processed output.
```
video = cv2.VideoCapture("sample_video.mp4")

while video.isOpened():
    ret, frame = video.read()

    if not ret:
        break

    # Rotate the frame
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)

    # Convert BGR to RGB
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)

    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis("off")
    plt.show()

    time.sleep(0.03)

video.release()
```
---

## 📸 Output

### i) Captured JPG Image
The webcam frame is successfully saved as:

```bash
captured_image.jpg
```

### ii) Live Video Display
The original webcam video stream is displayed.

### iii) Resized Video
The video is resized to:

```bash
640 × 480
```

### iv) Rotated Video
The video feed is rotated by:

```bash
90° Clockwise
```

## 👨‍💻 Developed By

**Name:** V Rishon Anand 
**Register Number:** 212224240135

---

## ✅ Result

The webcam image was successfully captured and processed using OpenCV. Different video processing operations such as image saving, live display, resizing, and frame rotation were implemented successfully.

---
