# AI-Based Image Classification System

A beginner-friendly college mini-project. Upload an image or capture one from your webcam, and an AI model (MobileNet, running in your browser with TensorFlow.js) tells you what object it sees and how confident it is.

## Features
- Image upload (JPG, PNG, WEBP)
- Live webcam capture
- Real MobileNet predictions (no fake or hardcoded results)
- Predicted object name + confidence percentage + top-3 list
- Shows the uploaded/captured image
- Clear / Reset button
- Error messages for camera permission, missing camera, model download failure
- Responsive layout (laptop and mobile), light and dark mode

## Project structure
```
ai-image-classifier/
├── index.html          <- the whole website (HTML + CSS + JavaScript)
├── README.md           <- this file
├── PROJECT_REPORT.md   <- report text for your college submission
└── TROUBLESHOOTING.md  <- fixes for common problems
```

## How to run
1. Save the code as `index.html` inside a folder.
2. **Recommended:** start a local server (the webcam only works on `localhost` or `https`).
   - **VS Code:** install the *Live Server* extension, right-click `index.html`, choose *Open with Live Server*.
   - **Python:** open a terminal in the folder and run `python -m http.server 8000`, then open `http://localhost:8000`.
3. Wait for the green message **"AI model ready"**, then upload an image or start the camera.

> An internet connection is needed the first time, because TensorFlow.js and the MobileNet model are downloaded from the internet.

## Technologies
HTML5, CSS3, JavaScript, TensorFlow.js 4.22.0, MobileNet 2.1.1 (trained on ImageNet, 1,000 classes).

## Limitations
- Only recognises the 1,000 ImageNet categories.
- Accuracy drops with blurry, dark, or cluttered photos.
- Low confidence means the model is unsure.
