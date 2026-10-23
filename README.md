# Phone Camera Hand Gesture Mouse Control 

Control your computer mouse using hand gestures and your phone's camera — built with Python, OpenCV, MediaPipe, and PyAutoGUI.

Unlike projects that rely on a built-in webcam, this project uses a phone camera connected to the computer and accessed through OpenCV.

## Features

- **Phone Camera Support:** Uses a connected phone camera as the input source.
- **Hand Tracking:** Detects and tracks hand landmarks in real time using MediaPipe.
- **Mouse Movement:** Move the cursor by moving your index finger.
- **Click:** Use a specific two-finger gesture to click.
- **Drag and Drop:** Hold a gesture to drag items and release it to drop them.
- **Scroll:** Scroll up and down using a hand gesture.
- **Smooth Cursor Movement:** Applies smoothing to make cursor movement less jittery.

## Built With

- Python
- OpenCV
- MediaPipe
- PyAutoGUI

## Requirements

- Python 3.11
- A computer running Python
- A phone camera connected to the computer
- The required Python libraries

## Installation

Install the dependencies:

```bash
pip install opencv-python mediapipe pyautogui
```

## Phone Camera Setup

This project uses camera index `3`:

```python
cam = cv2.VideoCapture(3)
```

The camera index depends on your system and how your phone camera is connected. You may need to change `3` to the appropriate index on your computer.

Make sure your phone camera is accessible to OpenCV before running the script.

## Run the Project

Save the code as `main.py` and run:

```bash
python main.py
```

Make sure your phone camera is connected and selected correctly.

Press `q` to close the camera window and stop the program.

## Gesture Controls

| Hand Gesture | Action |
|---|---|
| Move index finger | Move the cursor |
| Index and middle fingers open, ring and pinky closed | Click |
| Index and pinky open, middle and ring fingers closed | Drag and drop |
| Thumb open with other fingers closed | Scroll |

## How It Works

1. OpenCV captures frames from the connected phone camera.
2. MediaPipe detects hand landmarks in each frame.
3. The index finger position is mapped to the screen coordinates.
4. PyAutoGUI moves the cursor and performs mouse actions based on detected gestures.
5. Cursor smoothing and frame-based gesture detection help reduce unwanted movements and accidental actions.

## Notes

- Camera index `3` is specific to the current setup and may differ on other computers.
- Camera connection methods and setup steps depend on your phone, operating system, and camera application.
- Gesture recognition can be affected by lighting, camera angle, and hand position.
- PyAutoGUI controls the computer's actual mouse, so use the project carefully.

## 📄 License

This project is open source. Add a license file if you want others to reuse or modify your code under explicit terms.
