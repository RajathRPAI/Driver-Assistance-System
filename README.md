# Driver Assistance System

## Overview

The **Driver Assistance System** is an AI-powered application designed to enhance driver safety by detecting drowsiness and providing real-time alerts. It uses computer vision techniques to monitor the driver’s face and eyes, issuing warnings when signs of fatigue or distraction are detected.

## Features

- **Drowsiness Detection**: Uses a pre-trained deep learning model (`eye_status_model.h5`) to determine if the driver's eyes are closed.
- **Face & Eye Tracking**: Utilizes OpenCV and Haarcascade classifiers to monitor the driver’s face and eye movements.
- **Audio Alerts**: Plays an alert sound (`alert.mp3`) when drowsiness is detected.
- **Voice Assistance**: Provides real-time recommendations through voice notifications.
- **Emergency Messaging (Optional)**: May integrate with WhatsApp (via `PyWhatKit`) to send emergency alerts if needed.

## Installation

### Prerequisites

Ensure you have the following dependencies installed:

```sh
pip install opencv-python keras tensorflow numpy pywhatkit
```

### Setup

1. Clone the repository or extract the project files.
2. Ensure the required models and XML files (`eye_status_model.h5`, `haarcascade_eye.xml`, `haarcascade_frontalface_default.xml`) are in the project directory.
3. Run the main script:
   ```sh
   python detection-msg-recommend_voice-maps.py
   ```

## How It Works

1. The system captures real-time video from the webcam.
2. It detects the driver’s face and eyes using OpenCV.
3. If the eyes remain closed for a prolonged period, an alert sound is played.
4. The system may also send an emergency message via WhatsApp if configured.

## File Structure

- `detection-msg-recommend_voice-maps.py` - Main script for detection and alerts
- `eye_status_model.h5` - Pre-trained deep learning model for eye status detection
- `haarcascade_eye.xml` - OpenCV classifier for eye detection
- `haarcascade_frontalface_default.xml` - OpenCV classifier for face detection
- `alert.mp3` - Audio alert file
- `PyWhatKit_DB.txt` - (Optional) Used for messaging functionality

## Future Improvements

- Implement head pose estimation to detect driver distraction.
- Add fatigue level monitoring based on multiple facial features.
- Enhance alert mechanisms with more notification options.
- **Streamlit Integration for UI**: Develop a user-friendly web interface using Streamlit to display real-time detection results and alerts.

## License

This project is open-source and available for modification and enhancement.


For questions or contributions, feel free to open an issue or submit a pull request!

