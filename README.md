# Asistente Visual Rápido

**Asistente Visual Rápido** is an accessibility-focused web prototype that explores how computer vision and audio feedback can help people with visual impairments identify obstacles in their surroundings.

The interface uses a camera feed and an image-classification model to display predictions and provide spoken alerts.

> **Safety notice:** This project is an experimental prototype. It is not a certified mobility aid and must not replace a white cane, guide dog, orientation and mobility training, or other established safety tools. Never rely on it as the sole way to detect hazards.

## Features

- Camera input with front/rear camera switching on supported devices.
- Real-time image classification using TensorFlow.js and a Teachable Machine image model.
- Spoken alerts using the browser's speech synthesis capabilities.
- Audio beeps for obstacle warnings.
- Adjustable alert repetition interval, speech rate, and detection confidence threshold.
- High-contrast interface with live status updates.

## Getting Started

### Requirements

- A modern browser with camera support.
- Camera permission.
- A local web server such as the Live Server extension in Visual Studio Code.
- The trained model files in the `mi-modelo/` directory.

### Run Locally

1. Clone or download this repository.
2. Confirm that the `mi-modelo/` directory contains the model files:
   - `model.json`
   - `metadata.json`
   - `weights.bin` (or the weight file referenced by `model.json`)
3. Open the project folder in Visual Studio Code.
4. Start a local server with Live Server, or use another static web server.
5. Open the served page and allow camera access.
6. Press **Start Assistant** to load the model and begin camera-based predictions.

Opening the HTML file directly with a `file://` URL may prevent the browser from loading the model files. Use a local server instead.

## Built With

- HTML
- Tailwind CSS via CDN
- JavaScript
- TensorFlow.js
- Teachable Machine Image Library
- Web Audio API
- Web Speech API

## Model and Configuration

The application loads its model from the relative path `./mi-modelo/`. If the model cannot be loaded, check that all required files are present and that the page is being served over HTTP or HTTPS.

The confidence threshold, alert interval, and speech rate can be adjusted in the interface.

## Limitations

- Detection quality depends on the training data, lighting, camera quality, device performance, and model accuracy.
- Browser camera and audio permissions are required.
- Speech synthesis and camera switching behavior vary by browser and device.
- The prototype does not guarantee that every obstacle will be detected or correctly classified.

## Project Status

This is a learning and prototyping project. It should be tested in controlled environments and evaluated with accessibility specialists and intended users before any real-world deployment.

## Author

Developed as a learning project by **Andrea Rivas**.
