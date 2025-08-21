#Media Controlling using Hand Gesture

Technologies Used

Python

OpenCV (Computer vision & video capture)

MediaPipe (Hand tracking & landmark detection)

PyAutoGUI (Keyboard & mouse automation, screenshots)

NumPy (Array manipulation)

Time Module (Delay handling)

Project Description

This project enables touchless media control using hand gestures. By detecting the number of fingers raised in front of a webcam, it triggers system actions like volume control, navigation, and screenshot capture. It provides an intuitive and real-time interface for controlling media without touching any device.

Problem Statement

Traditional media control devices (keyboard, mouse, or touchscreen) can be inconvenient in scenarios like cooking, presentations, or gaming. This project solves the problem by using hand gestures to perform media actions, allowing hands-free interaction with the system.

Features & Functionalities

Detects hand gestures in real-time using webcam.

Maps finger count to actions:

1 finger: Increase volume

2 fingers: Decrease volume

3 fingers: Press “up” key

4 fingers: Press “down” key

5 fingers: Take a screenshot

Annotates live feed with hand landmarks.

Works with single-hand gestures and minimal delay.

Architecture & Workflow

Video Capture: OpenCV captures webcam feed.

Hand Detection: MediaPipe detects hand and landmarks.

Finger Counting: Calculate number of fingers raised.

Action Triggering: PyAutoGUI performs corresponding system action.

Display: Show annotated live video feed with hand landmarks.

WorkFlow : 

Webcam Feed → MediaPipe Hand Detection → Count Fingers → 
Map Finger Count → Trigger System Action → Show Video + Landmarks

Implementation Details

Finger Counting Logic: Calculates differences in landmark coordinates to determine fingers raised.

Debouncing: Ensures actions trigger only once per gesture using prev variable and 0.2-second delay.

Media Actions: Volume control, navigation, screenshot capture using PyAutoGUI.

Hand Landmark Drawing: Visual overlay of hand skeleton with mp.solutions.drawing_utils.draw_landmarks().

Challenges & Solutions

Flickering gestures: Multiple triggers for same gesture. Solution: Added delay and prev check.

Variations in hand size/angle: Thresholds based on landmark differences normalized to hand size.

Achievements & Novelty

Enables real-time touchless media control.

Provides intuitive and natural interaction.

Can be extended for custom gestures or more advanced controls.
