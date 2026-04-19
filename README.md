# Air Write (Gesture-Based Drawing System)

A real-time gesture-controlled drawing system that allows users to draw in the air using hand tracking via a webcam.

## Overview
This project uses computer vision to track hand movements and convert them into drawing input on a canvas. It supports multiple gestures for interaction and provides both local and cloud-based features.

## Features
- Draw in air using index finger tracking
- Gesture-based controls:
  - ☝️ Draw (index finger up)
  - 🤏 Lift pen (pinch)
  - ✋ Undo last stroke
  - ✊ Erase mode
- Real-time canvas rendering with smoothing
- Adjustable parameters:
  - Brush size
  - Opacity
  - Glow
  - Smoothing level
- Save drawings locally (PNG)
- Cloud storage using Firebase
- User authentication (login/signup)
- Personal gallery for saved drawings

## Tech Stack
- HTML, CSS, JavaScript
- MediaPipe Hands (hand tracking) :contentReference[oaicite:0]{index=0}
- Firebase (Authentication + Firestore) :contentReference[oaicite:1]{index=1}
- Canvas API

## How It Works
1. Webcam captures live video feed.
2. MediaPipe detects hand landmarks in real-time.
3. Finger positions are tracked and interpreted as gestures.
4. Coordinates are smoothed to reduce noise.
5. Drawing is rendered on canvas based on movement.
6. Optional: Data is saved locally or to Firebase.

## Challenges Faced
- **Shaky lines:** Hand tracking noise caused unstable drawing
- **Gesture accuracy:** Needed tuning of thresholds (pinch distance, confidence)
- **Real-time performance:** Balancing smoothness and responsiveness
- **False triggers:** Avoiding accidental erase/undo actions

## Improvements Made
- Implemented smoothing buffer for stable drawing
- Adjustable sensitivity and confidence thresholds
- Gesture hold logic (e.g., fist hold for erase)
- UI controls for fine-tuning behavior

## Future Improvements
- Multi-hand support
- Better stroke prediction (AI smoothing)
- Mobile support
- More gesture customization

## Usage
1. Open the website
2. Allow camera access
3. Use gestures to draw and interact
4. Save locally or to cloud

## Note
This project explores real-time gesture recognition, UI interaction, and integration of computer vision with web-based systems.
