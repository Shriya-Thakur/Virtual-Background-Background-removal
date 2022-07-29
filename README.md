# Virtual-Background-Background-removal

It is a Zoom and MsTeams like background changer/remover. You can remove and change your image or video background in real-time. Also added support for custom videos as background

# Prerequisite/libraries

#OpenCv

#Python 

#Numpy 

#MediaPipe 

#Os

# Input

Video Stream

# Output

New Video Stream with Virtual Background

# How it Works

Selfie Segmentation segments the prominent humans in the scene. It can run in real-time on laptops. The intended use cases include selfie effects and video conferencing, where the person is close (< 2m) to the camera.

1.Read in the live frame.

2.Read in the replacement frame(background) 

3.Pass the Frame through machine learning model.

4.Dilate the thresholded frame.

5.Find Contoures in the dilated frame.

6.Optimize/process the contours.

7.Draw(fill) the contour => this will be the foreground roi.

8.Separate the foreground from Background (cv.bitwize_and).

9.Remove the foreground Roi from the New Background (cv.bitwize_and(inverseRoi, NewBackground).

10.Combine the New Background Roi and foreground Roi (cv.bitwize_or(NewBackground, Foreground)
