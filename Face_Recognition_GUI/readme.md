# Face Recognition Login System

This project implements a Face Recognition-based Login and User Registration system using Python, `tkinter`, `OpenCV`, and `Pillow`. The system allows users to log in via face recognition and register new users by capturing their facial data.

## Features
- **Webcam Integration**: Displays live webcam feed in the main window.
- **Login via Face Recognition**: Recognizes and logs in registered users via facial recognition.
- **New User Registration**: New users can register by entering their username and capturing their face.
- **User Log**: Login attempts are logged with the username and timestamp in a log file.
- **Error Handling**: Prompts users to either register or retry if an unrecognized face is detected.

## Requirements

Before running the project, ensure you have the following Python packages installed:

- `tkinter` - for creating the graphical user interface (GUI).
- `opencv-python` - for capturing and processing webcam images.
- `Pillow` - for image processing and manipulation.
- `numpy` - for array operations.
- `subprocess` - for running external processes like the `face_recognition` tool.

You can install these dependencies using pip:

```bash
pip install opencv-python pillow numpy

pip install face_recognition

.
├── db/                # Directory for storing registered users' face images
├── log.txt            # Log file storing login events (username and timestamp)
├── tmp.jpg            # Temporary image used for face recognition during login
├── app.py             # Main Python application file
└── util.py            # Utility functions for GUI components (buttons, labels, etc.)

python app.py
username, timestamp


You can copy and paste this into your `README.md` file in the project directory. It will provide a structured guide for anyone using or contributing to the project.

