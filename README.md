DROWSY DRIVER DETECTION:

The code detects driver drowsiness by analyzing the Eye Aspect Ratio (EAR):
1. Face & Eye Detection: Uses dlib to detect the face and eye landmarks in real-time.
2. EAR Calculation: Measures vertical and horizontal distances of eye landmarks. EAR decreases when eyes are closed.
3. Threshold Check: If EAR stays below a set threshold (e.g., 0.19) for a specific duration, it flags the driver as drowsy.
4. Alert: Displays a warning ("DROWSY") on the screen and logs it in the terminal.

dataset : https://github.com/davisking/dlib-models/raw/refs/heads/master/shape_predictor_68_face_landmarks.dat.bz2

add the path of the extracted dataset in : dlib_facelandmark = dlib.shape_predictor("path_name")

To run the drowsiness detection system, you need the following requirements:

1. Python
Version: Python 3.x (recommended: Python 3.6 or higher)

2. Libraries and Dependencies
You can install the required libraries using pip. These libraries are essential for image processing, face detection, and machine learning:
OpenCV: For real-time image and video processing.
  pip install opencv-python
dlib: For detecting face landmarks and calculating the Eye Aspect Ratio (EAR).
  pip install dlib
scipy: For calculating Euclidean distances (used in EAR calculation).
  pip install scipy

3. Shape Predictor Model
File: shape_predictor_68_face_landmarks.dat
Download the model from the dlib website.
This file is used for detecting facial landmarks (like eyes, nose, and mouth).
