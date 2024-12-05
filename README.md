DROWSY DRIVER DETECTION:

The code detects driver drowsiness by analyzing the Eye Aspect Ratio (EAR):
1. Face & Eye Detection: Uses dlib to detect the face and eye landmarks in real-time.
2. EAR Calculation: Measures vertical and horizontal distances of eye landmarks. EAR decreases when eyes are closed.
3. Threshold Check: If EAR stays below a set threshold (e.g., 0.19) for a specific duration, it flags the driver as drowsy.
4. Alert: Displays a warning ("DROWSY") on the screen and logs it in the terminal.

dataset : https://github.com/davisking/dlib-models/raw/refs/heads/master/shape_predictor_68_face_landmarks.dat.bz2

add the path of the extracted dataset in : dlib_facelandmark = dlib.shape_predictor("path_name")
