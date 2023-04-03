
# Intruder Detection System in OpenCV

This program is an implementation of an Intruder Detection System using OpenCV (Open Source Computer Vision Library). It uses video frames captured from a camera, analyses the frames to detect motion within a designated area, and alerts the user if any object enters the designated area.

The program allows the user to select a rectangular area within the frame where the motion detection is to be performed. Once the user selects the area, any object that enters or moves within that area will be detected and highlighted.



## Tools and Libraries

- Python
- VS Code
- OpenCV
- NumPy


## Program Flow

- Import necessary libraries - OpenCV and NumPy.
- Define a function called click_event that handles mouse events (click, move, and release) within the selected rectangular area. The function sets the coordinates of the selected rectangle and the draw variable, which is used to indicate whether to draw a rectangle or not.
- Create a global variable called draw and initialize it to zero. Also, create two more global variables called frame1 and rect.
- Create a VideoCapture object that captures the video feed from the camera.
- Read the first two frames and store them in variables frame1 and frame2.
- Display the first frame and set the mouse callback function to click_event.
- Start a loop that reads frames from the camera until the program is terminated.
- Calculate the absolute difference between frame1 and frame2.
- Convert the difference to grayscale and apply Gaussian blur to remove noise.
- Threshold the blurred image and apply dilation to make the white regions more prominent.
- Crop the dilated image to the selected rectangular area.
- Find contours within the cropped image and draw bounding rectangles around them.
- Display the processed frames along with any bounding rectangles and text.
- Set frame1 to frame2 and read the next frame.
- Terminate the loop if the user presses the Esc key.
- Release the VideoCapture object and destroy all windows.


## Functionality

The program first prompts the user to select a rectangular area where motion detection is to be performed. To do this, the user clicks the left mouse button on the desired starting point of the rectangle and then drags the mouse to the opposite corner of the rectangle. Once the mouse is released, the program stores the dimensions of the rectangle in the rect variable and begins detecting motion within the selected area.

The program then reads frames from the camera, calculates the absolute difference between consecutive frames, and applies thresholding and dilation to highlight the areas of motion. The resulting binary image is then cropped to the selected rectangular area.

Contours are then identified within the cropped image, and bounding rectangles are drawn around them. The program also checks the area of each contour and only draws bounding rectangles for those with an area greater than 300 pixels. If a bounding rectangle is drawn, the program displays the text "Intruder Detected" on the frame.

Finally, the program displays the processed frames along with any bounding rectangles and text. The program continues to read frames until the user terminates it by pressing the Esc key.



##Future Scope
This project can be further extended to include additional features such as face recognition, crowd analysis, and automatic tracking of detected objects. The system can also be integrated with alarms or notifications to alert security personnel in real-time. Additionally, the project can be optimized for high-performance systems and deployed for commercial use in public areas, workplaces, and other places requiring advanced video surveillance.

