# Air-Canvas

Air Canvas is an interactive drawing application that uses computer vision to create a virtual painting experience. Built with OpenCV and Python, this project allows users to draw on a digital canvas using hand gestures captured by a webcam.

## Features:

- Real-time color tracking and drawing
- Multiple color options: Blue, Green, Red, and Yellow
- Clear canvas functionality
- Adjustable color detection via trackbars
- Live video feed with color selection interface

## Technical Implementation:

### OpenCV Integration:
The project leverages OpenCV's powerful computer vision capabilities for:
- Video capture and processing
- Color space conversion (BGR to HSV)
- Drawing shapes and text on frames
- Image manipulation and filtering

### Color Detection and Masking:
- Uses HSV (Hue, Saturation, Value) color space for robust color detection
- Implements dynamic color thresholding using trackbars
- Creates a binary mask to isolate the drawing tool from the background

### Contour Detection:
- Applies morphological operations to enhance the mask
- Utilizes OpenCV's contour finding algorithms to detect the drawing tool
- Identifies the largest contour as the active drawing point

### Drawing Mechanism:
- Employs `collections.deque` for efficient storage and management of drawing points
- Implements smooth line drawing between consecutive points

## How it works:

1. The application uses your webcam to track a colored object (like a marker or your fingertip).
2. Move the object in front of the camera to draw on the virtual canvas.
3. Select different colors by moving the object to the color buttons at the top of the frame.
4. Clear the canvas by selecting the "CLEAR ALL" button.
5. Adjust color detection parameters using the trackbars for optimal performance in different lighting conditions.

This project demonstrates the power of computer vision in creating intuitive and engaging user interfaces, bridging the gap between physical gestures and digital art creation. It showcases practical applications of image processing techniques, contour analysis, and real-time video manipulation using OpenCV.
