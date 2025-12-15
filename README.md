# Hand Gesture Recognition for Internship Task

## Overview
This project demonstrates hand gesture recognition using **MediaPipe** and **OpenCV**. The program tracks hand landmarks and detects various hand gestures such as **LIKE (Thumbs-up)**, **DISLIKE (Thumbs-down)**, **OK (👌)**, **PEACE (✌️)**, **CALL ME (🤙)**, **STOP (✋)**, **FORWARD (👆)**, **LEFT (👈)**, **RIGHT (👉)**, and **I LOVE YOU (🤟)** based on hand positions and finger movements.

The solution uses **MediaPipe**'s hand tracking model to detect 21 landmarks on the hand and uses simple rules based on their relative positions to identify the gestures. The project involves real-time hand tracking using a webcam.

## Project Files

- **main.py**: The Python script that performs hand gesture recognition and displays the detected gestures.
- **hand-landmarks (1).png**: Image showing the hand landmarks for reference.

## Requirements

To run this project, you need the following libraries:

- **OpenCV**: For video capture and image processing.
- **MediaPipe**: For hand landmark detection and tracking.

You can install the necessary libraries using `pip`:
pip install opencv-python mediapipe

How the Code Works:
1.Initialize MediaPipe Hands:
MediaPipe is used to track hand landmarks. The hand landmarks are detected with a minimum detection confidence of 0.5 and a minimum tracking confidence of 0.5.

2.Webcam Feed:
The program uses your webcam to capture the frames in real-time. It processes each frame to detect hand landmarks.

3.Gesture Recognition:
The program checks for specific hand gestures by analyzing the relative positions of the landmarks. It recognizes several gestures such as thumbs-up, peace, stop, and more based on predefined conditions for each gesture.

4.Gesture Display:
When a gesture is detected, the corresponding gesture name is displayed on the screen (e.g., "LIKE", "STOP").

Gesture Detection:

1.LIKE (Thumbs-up): The thumb is extended upwards while all other fingers are folded.
2.DISLIKE (Thumbs-down): The thumb is extended downwards while all other fingers are folded.
3.OK (👌): The thumb and index finger are close together.
4.PEACE (✌️): The thumb, ring, and pinky fingers are close, with index and middle fingers extended.
5.CALL ME (🤙): The index, middle, and pinky fingers are folded, and the thumb and pinky are extended with a significant distance between them.
6.STOP (✋): All fingers are extended.
7.FORWARD (👆): The index finger is extended upwards, and all other fingers are folded.
8.LEFT (👈): The thumb is extended upwards, and all other fingers are folded with specific X/Y positioning for the hand.
9.RIGHT (👉): Similar to LEFT gesture but mirrored.
10.I LOVE YOU (🤟): The index finger is extended, the thumb is extended, and the pinky is raised with the middle and ring fingers folded.

How to Run the Code:

1.Clone the repository:
git clone https://github.com/your-username/hand-gesture-recognition.git

2.Navigate to the project directory:
cd hand-gesture-recognition

3.Install dependencies:
pip install opencv-python mediapipe

4.Run the main.py script:
python main.py

The program will start capturing the webcam feed and detecting hand gestures in real-time. If a gesture is detected, it will be displayed on the screen.

5.Exit the program by pressing q on your keyboard.

Example Output:
The program will display the detected gesture on the screen. For example:
LIKE👍 gesture detected
