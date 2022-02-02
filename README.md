# LicensePlateDetection_Recognition

  License plate detection & recognition is a technique that needs to be used in daily life
activities such as detecting license plates of vehicles that exceed the speed in traffic and/or in
smart parking systems. It aims to extract and recognize the characters on license plates by
performing image processing and pattern recognition. In this project, it is aimed to implement
such a technique that will be used in the cases where the license detection is needed. There will
be four main steps in the implementation.

 These are:
1) Detecting the license plate
2) Processing the cropped license plate image to prepare it for recognition
3) Segmenting and extracting the characters on the plate
4) Applying Optical Character Recognition (OCR) to recognize the characters.

  For the first task, it is decided to use yolov4 to perform detection. YOLO (You Only 
Look Once) is a state-of-the-art, real time object detection algorithm. With yolov4, it is aimed to train 
custom model using a car plate dataset in Kaggle and then detect the plate locations in a frame 
with this model for further processing. The license plate detection is also performed without 
using yolov4 in the project, the difference between the performances is compared in the project.
  To prepare the license plate for the segmentation part, some processing should be 
performed such as noise smoothing and thresholding. For this mission, OpenCV is used which 
is a real-time optimized computer vision library. With OpenCV, various tasks can be performed 
like binarization, blur and edge detection. 
  For segmentation, there are two approaches that are used in the project. The first one is 
to detect contours and use them for segment the characters from each other. The other one is 
histogram approach. By following the intensity changes in the cropped image, which is a 
binarized license plate, the characters are separated. Both approaches are used together in the 
implementation. Optical Character Recognition systems transform two dimensional images of text into 
machine-readable text. OCR is performed by using EasyOCR library and pyTesseract libraries.

This project is the term group project of EE 417(Computer Vision) course.
