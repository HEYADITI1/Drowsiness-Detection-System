# Driver Drowsiness Detection System
This project implements a driver drowsiness detection system using Python, OpenCV, and Dlib. It monitors the driver's eyes and alerts when signs of drowsiness are detected.

## Applications
### This can be used by riders who tends to drive the vehicle for a longer period of time that may lead to accidents
## Code Requirements
### The example code is in Python ([version 3.8](https://www.python.org/download/releases/3.8/) or higher will work).
## Dependencies
1)import cv2
 2)import immutils
 3)import dlib
 4)import scipy
 5)import playsound
 6)import queue
 7)import time
 8)import sys

## Description
###  A computer vision system made with the help of opencv that can automatically detect driver drowsiness in a real-time video stream and then play an alarm if the driver appears to be drowsy.
## Algorithm
● We utilised a pre trained frontal face detector from Dlib’s library which is based on  a modification to the Histogram of Oriented Gradients in combination with Linear  SVM for classification.  

● The pre-trained facial landmark detector inside the dlib library is used to estimate  the location of 68 (x, y)-coordinates that map to facial structures on the face. The 68  landmark output is shown in the figure below. However, we utilised the 70 landmark  model.

![eye_aspect_ratio](https://github.com/user-attachments/assets/5f826b24-6e92-449c-a395-0a377e90e9e1)

● We then calculate the aspect ratio to check whether eyes are opened or closed.

● The eye is open if Eye Aspect ratio is greater than threshold. (Around 0.3)

![eye](https://github.com/user-attachments/assets/d672f51e-091a-4f96-9bcc-208e717622e6)

● A blink is supposed to last 200-300 milliseconds.

● A drowsy blink would last for  800-900  ms. 

![face](https://github.com/user-attachments/assets/f382692a-984f-474a-a980-cbcbb4c7c28e)

## Execution
To run the code, run 

python blinkDetect.py
