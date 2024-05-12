# Finger Count Using OpenCV

## Description

The project aims to count the number of fingers inside a **region of interest (ROI)** using concepts of computer vision and **convex hull algorithm**. It utilizes the [OpenCV](https://en.wikipedia.org/wiki/OpenCV) library to implement techniques such as [image thresholding](https://en.wikipedia.org/wiki/Thresholding_(image_processing)), [contour detection](https://en.wikipedia.org/wiki/Contour_detection), drawing on a live camera feed, and image segmentation. To count the number of fingers inside the ROI, the convex hull algorithm is utilized.

## Project Flow

1. **Global Variables Definition**:
   - Declare global variables to be updated dynamically throughout the program execution.

2. **Frame Reading Function**:
   - Create a function to capture frames directly from the live camera.

3. **Image Thresholding**:
   - Apply image thresholding on the captured frame to separate the foreground (hand) within the ROI from the background. 
   - Image thresholding is a technique used to segment images, distinguishing objects or features from the background by converting grayscale images to binary images based on intensity levels.

4. **Contour Detection**:
   - Implement contour detection on the thresholded frames obtained from the camera feed.
   - Contour detection involves identifying and extracting the boundaries of objects in an image.

5. **Convex Hull Algorithm**:
   - Utilize the [convex hull algorithm](https://en.wikipedia.org/wiki/Convex_hull) to calculate the extreme points or outermost boundary of the hand within the ROI.
   - The convex hull of a set of points in the Euclidean plane is the smallest convex polygon that encloses all points in the set.
   - Refer to [OpenCV Convex Hull Documentation](https://docs.opencv.org/4.x/d7/d1d/tutorial_hull.html) for implementation details.

6. **Extreme Points Identification**:
   - Index the output from the convex hull to obtain the coordinates of the extreme top, bottom, left, and right corners of the hand within the ROI.

7. **Palm Bounds Definition**:
   - Determine the center of the hand and draw a circle to define the bounds of the palm.

8. **Finger Counting**:
   - Count the extended fingers outside the bounds of the palm to determine the total number of fingers.

## Video Demonstration

https://img.youtube.com/vi/Finger%20Count%202024-05-12%2015-58-18/0.jpg

## References

- [OpenCV Documentation](https://docs.opencv.org/4.x/index.html)
- [Convex Hull Wikipedia](https://en.wikipedia.org/wiki/Convex_hull)
- [Contour Detection Wikipedia](https://en.wikipedia.org/wiki/Contour_detection)
- [Image Thresholding Wikipedia](https://en.wikipedia.org/wiki/Thresholding_(image_processing))
