# ImageRecognition



OpenCV is the huge open-source library for computer vision, machine learning, and image processing and now it plays a major role in real-time operation which is very important in today’s systems. By using it, one can process images and videos to identify objects, faces, or even the handwriting of a human. This article focuses on detecting objects.

Note: For more information, refer to Introduction to OpenCV.
Object Detection

Object Detection is a computer technology related to computer vision, image processing, and deep learning that deals with detecting instances of objects in images and videos. We will do object detection in this article using something known as haar cascades.
Haar Cascades

Haar Cascade classifiers are an effective way for object detection. This method was proposed by Paul Viola and Michael Jones in their paper Rapid Object Detection using a Boosted Cascade of Simple Features. Haar Cascade is a machine learning-based approach where a lot of positive and negative images are used to train the classifier.

    Positive images – These images contain the images that we want our classifier to identify.
    Negative Images – Images of everything else, which do not contain the object we want to detect.

Steps to download the requirements below

    Run The following command in the terminal to install opencv.

    pip install opencv-python

    Run the following command to in the terminal install the Matplotlib.

    pip install matplotlib

    To download the haar cascade file and image used in the below code as a zip file click here.

Note: Put the XML file and the PNG image in the same folder as your Python script.
Implementation
Image used

python-opencv-detect-image
Opening an image
Python3

import cv2
from matplotlib import pyplot as plt
  
  
# Opening image
img = cv2.imread("image.jpg")
  
# OpenCV opens images as BRG 
# but we want it as RGB and 
# we also need a grayscale 
# version
img_gray = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY)
img_rgb = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
  
# Creates the environment 
# of the picture and shows it
plt.subplot(1, 1, 1)
plt.imshow(img_rgb)
plt.show()

