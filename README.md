# 📸 Face Recognition Attendance System

A real-time face recognition-based attendance system using OpenCV and LBPH (Local Binary Patterns Histograms) face recognizer. This project detects faces from a webcam feed, matches them against known faces, and marks attendance with timestamps.

## 🚀 Features

- **Real-time Face Detection:** Uses OpenCV's Haar Cascade to detect faces from webcam input.
- **Face Recognition:** Implements LBPH face recognizer for identifying faces.
- **Attendance Marking:** Automatically logs names and timestamps when a recognized face is detected.
- **Dynamic Labeling:** Reads known faces from a directory and assigns labels based on filenames.
- **Efficient Tracking:** Ensures each name is logged only once per session.

## 📁 Project Structure

```
/attendance
│-- /known_faces           # Folder containing images of known individuals (jpg/png)
│-- face_recognition.py    # Main Python script
│-- README.md              # Project documentation
```

## ⚙️ Requirements

Ensure you have the following installed:

- Python 3.x
- OpenCV
- NumPy

Install dependencies using:

```bash
pip install opencv-python numpy
```

## 📸 How to Use

1. **Prepare Known Faces:**
   - Add images of known individuals in the `known_faces` folder.
   - Ensure filenames reflect the names (e.g., `JohnDoe.jpg`).

2. **Run the script:**

```bash
python face_recognition.py
```

3. **Using the Webcam:**
   - The webcam will open and start detecting faces.
   - Recognized names and timestamps will be printed to the console.

4. **Stop the program:**
   - Press **'q'** to quit the webcam feed.

## 📦 Code Overview

- **Face Loading & Labeling:**
  Reads images from the `known_faces` directory, detects faces, and assigns labels for training the recognizer.

- **Face Recognition:**
  Uses LBPH to train a model and predict faces detected in real-time.

- **Attendance Marking:**
  Ensures each name is only logged once using a set to track recognized faces.

## 🏷️ Sample Code Snippet

```python
# Mark attendance with timestamp
from datetime import datetime

def mark_attendance(name):
