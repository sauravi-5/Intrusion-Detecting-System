# Intruder Detection System in OpenCV
This program is an implementation of an Intruder Detection System using OpenCV (Open Source Computer Vision Library). It uses video frames captured from a camera, analyses the frames to detect motion within a designated area, and alerts the user if any object enters the designated area.

The program allows the user to select a rectangular area within the frame where the motion detection is to be performed. Once the user selects the area, any object that enters or moves within that area will be detected and highlighted.

<h1>Requirements</h1>
*OpenCV
*NumPy

<h1>Program Flow</h1>
*Import necessary libraries - OpenCV and NumPy.

*Define a function called click_event that handles mouse events (click, move, and release) within the selected rectangular area. The function sets the coordinates of the selected rectangle and the draw variable, which is used to indicate whether to draw a rectangle or not.

*Create a global variable called draw and initialize it to zero. Also, create two more global variables called frame1 and rect.

*Create a VideoCapture object that captures the video feed from the camera.

*Read the first two frames and store them in variables frame1 and frame2.

*Set the rect variable to the dimensions of the first frame.

*Display the first frame and set the mouse callback function to click_event.

*Start a loop that reads frames from the camera until the program is terminated.

*Calculate the absolute difference between frame1 and frame2.

*Convert the difference to grayscale and apply Gaussian blur to remove noise.

*Threshold the blurred image and apply dilation to make the white regions more prominent.

*Crop the dilated image to the selected rectangular area.

*Find contours within the cropped image and draw bounding rectangles around them.

*Display the processed frames along with any bounding rectangles and text.

*Set frame1 to frame2 and read the next frame.

*Terminate the loop if the user presses the Esc key.

*Release the VideoCapture object and destroy all windows.

<h1>Conclusion</h1>
This program demonstrates the basics of motion detection and object tracking in OpenCV. The use of a rectangular area allows for more targeted motion detection, and the program could be easily extended to include more advanced features, such as face detection or object recognition.
