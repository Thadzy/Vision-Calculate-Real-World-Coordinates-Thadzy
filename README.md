# Vision-Calculate-Real-World-Coordinates-Thadzy

# Camera Calibration and Object Tracking with OpenCV

This project provides a set of Python scripts to perform camera calibration, object tracking, and image capture using OpenCV. It also includes the functionality to undistort captured images based on previously saved camera calibration data.

## Features

1. **Camera Calibration**:
    - Detects checkerboard corners from a set of images.
    - Calculates camera matrix, distortion coefficients, rotation vectors, and translation vectors.
    - Saves the calibration data to be used for later image undistortion.

2. **Image Capture with Webcam**:
    - Allows capturing images from a webcam.
    - Saves captured images with a simple keypress interface (`s` to save, `q` to quit).

3. **Object Tracking**:
    - Tracks blue-colored objects in real-time using HSV color space.
    - Draws contours and circles around the detected object.
    - Displays object position on the screen.

4. **Undistortion of Images**:
    - Loads camera calibration data and undistorts images to remove lens distortion.
    - Optionally crops the image to the valid region of interest (ROI).

## Prerequisites

- Python 3.x
- OpenCV
- NumPy

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/camera-calibration-object-tracking.git
    cd camera-calibration-object-tracking
    ```

2. Install required dependencies:
    ```bash
    pip install numpy opencv-python
    ```

3. Ensure you have a webcam connected to your machine.

## How to Use

### 1. Camera Calibration

To perform camera calibration, place a checkerboard pattern in view and capture multiple images using a camera. The checkerboard used here has dimensions `6x9`.

1. Place your calibration images inside the `./images` directory.
2. Run the calibration script:
    ```bash
    python calibrate_camera.py
    ```
3. Calibration data will be saved in `calibration_data.npz` for later use.

### 2. Capture Images with Webcam

To capture images from the webcam:

1. Run the webcam capture script:
    ```bash
    python capture_image.py
    ```
2. Press `s` to save an image, or press `q` to quit.

### 3. Object Tracking

To track blue-colored objects in real time:

1. Run the object tracking script:
    ```bash
    python object_tracking.py
    ```
2. The script will display the position of the detected object.

### 4. Undistort Images

To undistort a saved image using the camera calibration data:

1. Place the image to be undistorted in the `./images` directory.
2. Run the undistortion script:
    ```bash
    python undistort_image.py
    ```

## Example Commands

1. **Calibrate Camera**:
    ```bash
    python calibrate_camera.py
    ```

2. **Capture Image from Webcam**:
    ```bash
    python capture_image.py
    ```

3. **Track Object (Blue)**:
    ```bash
    python object_tracking.py
    ```

4. **Undistort Image**:
    ```bash
    python undistort_image.py
    ```

## File Structure

```
.
├── calibrate_camera.py       # Camera calibration script
├── capture_image.py          # Webcam image capture script
├── object_tracking.py        # Object tracking based on color
├── undistort_image.py        # Image undistortion script
├── images/                   # Folder containing images
├── README.md                 # Project documentation
└── calibration_data.npz      # Saved calibration data (generated after calibration)
```

## License

This project is licensed under the MIT License.

---
