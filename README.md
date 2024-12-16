# air-canvas
This Python script implements a simple virtual painting application using **OpenCV** and a webcam. Here's a summary:

### Features:
1. **Trackbars for Color Detection**:
   - Users can adjust the HSV (Hue, Saturation, and Value) thresholds for detecting the "pointer" (e.g., a colored object like a pen cap or marker).

2. **Drawing Colors**:
   - The app supports drawing in four colors: **Blue**, **Green**, **Red**, and **Yellow**. Buttons on the screen allow the user to select a color.

3. **Canvas and Interface**:
   - A virtual canvas is created for drawing. The top of the frame includes buttons for:
     - **CLEAR**: Erases the canvas.
     - Color buttons to switch between Blue, Green, Red, and Yellow.

4. **Pointer Detection**:
   - The script detects the pointer's position using a mask created by the HSV range.
   - The detected pointer is used to draw lines on the canvas.

5. **Contour Detection**:
   - Uses contour detection to identify the pointer, calculates its center, and tracks its movement.

6. **Drawing Logic**:
   - Keeps track of points for each color using **deques** (from the `collections` module).
   - Draws continuous lines between detected pointer positions.

7. **Windows Display**:
   - Displays three windows:
     - **Tracking**: The live webcam feed with the interface.
     - **Paint**: The virtual canvas.
     - **Mask**: The binary mask of the detected pointer.

8. **Quit Option**:
   - Pressing the **'q'** key exits the application.

### Libraries Used:
- `cv2` (OpenCV): For video capture, image processing, and GUI elements.
- `numpy`: For matrix operations.
- `collections.deque`: To manage points for drawing.

### Application Flow:
1. The webcam captures frames, which are flipped for a mirror effect.
2. The HSV mask identifies the colored pointer.
3. Pointer movements draw lines on the virtual canvas.
4. Users can select colors or clear the canvas using the buttons.

This program is a fun, interactive way to experiment with OpenCV, HSV color space, and basic drawing on images.
