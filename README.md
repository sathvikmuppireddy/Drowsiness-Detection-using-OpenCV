Drowsiness Detection System
This repository contains a Python script for detecting drowsiness using OpenCV and dlib libraries. 
The script utilizes facial landmarks to calculate the eye aspect ratio (EAR) and determine if the user is exhibiting signs of drowsiness.

Usage
Install Required Libraries:
pip install opencv-python imutils dlib

Run the Script:
python Drownsiness_detection.py

Adjust parameters (optional):
earThresh: Threshold value for EAR below which drowsiness is detected.
earFrames: Number of consecutive frames with low EAR to trigger the drowsiness alert.
shapePredictor: Path to the shape predictor file (default: "shape_predictor_68_face_landmarks").
Functionality
Facial Landmark Detection: Uses dlib's facial landmark detector to find 68 points on the face.
Eye Aspect Ratio Calculation: Calculates the ratio of the distance between the eye's vertical landmarks.
Drowsiness Detection: Detects drowsiness based on the EAR threshold and the number of consecutive frames with low EAR.
Alert Generation: Plays a sound alert when drowsiness is detected.

How it Works
->The script works by:
->Capturing video frames from the webcam.
->Detecting faces in each frame using dlib's face detector.
->Extracting facial landmarks for each detected face.
->Calculating the EAR for each eye.
->Monitoring the EAR values and detecting drowsiness based on the pre-defined thresholds.
->Generating an alert when drowsiness is detected.
