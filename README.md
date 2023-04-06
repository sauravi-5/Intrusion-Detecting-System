
# Intruder Detection System in OpenCV

This program is an implementation of an Intruder Detection System using OpenCV (Open Source Computer Vision Library). It uses video frames captured from a camera, analyses the frames to detect motion within a designated area, and alerts the user if any object enters the designated area.

The program allows the user to select a rectangular area within the frame where the motion detection is to be performed. Once the user selects the area, any object that enters or moves within that area will be detected and highlighted by playing an alert sound.



## Tools and Libraries

- Python
- VS Code
- OpenCV
- NumPy 
- Winsound
- Threading


## Contents of this repository
```bash
 Intrusion-Detection-System/
├─ code.py
├─ video.mp4
├─ LICENSE
├─ README.md
├─ requirements.txt
```
- *code.py* : Contains the code for the entire project.
- *video.mp4* : This is the file we have tested our code on.
- *requirements.txt* : This file has information about the `conda` environment used to create this project.


## Functionality

The program first prompts the user to select a rectangular area where motion detection is to be performed. To do this, the user clicks the left mouse button on the desired starting point of the rectangle and then drags the mouse to the opposite corner of the rectangle. Once the mouse is released, the program stores the dimensions of the rectangle in the `rect` variable and begins detecting motion within the selected area.

The program then reads frames from the camera, calculates the absolute difference between consecutive frames, and applies thresholding and dilation to highlight the areas of motion. The resulting binary image is then cropped to the selected rectangular area.

Contours are then identified within the cropped image, and bounding rectangles are drawn around them. The program also checks the area of each contour and only draws bounding rectangles for those with an area greater than 300 pixels. If a bounding rectangle is drawn, the program displays the text "Intruder Detected" on the frame. Additionally, a sound alert is played on Windows devices.

Finally, the program displays the processed frames along with any bounding rectangles and text. The program continues to read frames until the user terminates it by pressing the `Esc` key.


## How to Run the Code

1) Install the necessary libraries from requirements.txt
2) Create a virtual environment and activate.
3) To run this code input the following in terminal:

```bash
 python code.py
```
4) Initialize the first frame and select the area of interest. Then press Enter to get the output.


## Future Scope

This project can be further extended to include additional features such as face recognition, crowd analysis, and automatic tracking of detected objects. The system can also be integrated with notifications to alert security personnel in real-time. Additionally, the project can be optimized for high-performance systems and deployed for commercial use in public areas, workplaces, and other places requiring advanced video surveillance.

