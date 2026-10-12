<div align="center">

# GesturePilot AI

### Touchless presentation control with hand gestures

Control PowerPoint and PDF presentations using your webcam—no clicker or keyboard required.

</div>

---

## Overview

**GesturePilot AI** is a browser-based presentation controller that uses computer vision to recognize hand gestures and navigate slides hands-free. Upload a `.pptx` or `.pdf` file, enable your webcam, and control the presentation with simple gestures.

## Features

- **Five-gesture control** for common presentation actions.
- **PowerPoint support** for `.pptx` files.
- **PDF support** for `.pdf` presentations and documents.
- **Webcam-based hand tracking** powered by MediaPipe Tasks Vision.
- **Demo presentations** to try the app without preparing a file.
- **Presentation controls** including slide navigation, fullscreen, and a reversible black-screen mode.
- **Local processing for camera input**: webcam frames are processed in the browser and are not uploaded by the gesture-control feature.
- **Dark, responsive interface** with a gesture guide and on-screen webcam HUD.

> **Note:** Legacy `.ppt` files are not supported. Save them as `.pptx` or export them to PDF first.

## Gesture controls

| Gesture | Action |
| --- | --- |
| 🖐️ Open palm | Next slide |
| ✌️ V sign | Previous slide |
| 👍 Thumbs up | Toggle fullscreen |
| ✊ Closed fist | Exit presentation mode |
| ☝️ Index finger pointing up | Toggle the black-screen overlay |

Hold a gesture steadily for approximately **600 ms**. Return your hand to a neutral position before repeating a gesture to avoid accidental repeated actions. You can review the in-app **Five-Gesture Guide** for the current instructions.

## Tech stack

- React
- TypeScript
- Vite
- MediaPipe Tasks Vision
- PDF.js
- JSZip
- Lucide React
- Tailwind CSS

## Requirements

- Node.js and npm
- A modern browser (Chrome or Edge recommended)
- A webcam
- Permission to access the camera
- A `.pptx` or `.pdf` presentation, or use the built-in demo

## Run locally

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
cd YOUR-REPOSITORY
```

Replace `YOUR-USERNAME/YOUR-REPOSITORY` with your GitHub repository URL.

### 2. Install dependencies

```bash
npm install
```

### 3. Start the development server

```bash
npm run dev
```

Open the local URL printed in the terminal. This project is configured to use port **3000** by default.

### 4. Build for production

```bash
npm run build
```

To preview the production build locally:

```bash
npm run preview
```

To run the TypeScript checks:

```bash
npm run lint
```

## How to use

1. Start GesturePilot AI and open it in your browser.
2. Select **Try Demo** or upload a `.pptx` or `.pdf` file.
3. Allow camera access when your browser asks.
4. Position your hand clearly inside the webcam view.
5. Hold one of the supported gestures until the action triggers.
6. Use the gesture guide if you need a reminder of the controls.

**Camera troubleshooting:** If the camera does not start, check browser permissions, close other apps that may be using the webcam, and reload the page. Camera access generally requires `localhost` or a secure HTTPS connection.

## Privacy

Gesture recognition runs in the browser, and webcam frames used for gesture control are not uploaded by that feature. Your browser will ask for camera permission before the camera can be used.

Only open presentations you trust. The app parses uploaded presentation files locally in the browser.

## Project structure

```text
.
├── src/
│   ├── components/       # Home screen, viewer, gesture guide and overlays
│   ├── services/         # Gesture engine, PDF/PPTX parsing and demo data
│   ├── types/            # Presentation and gesture types
│   ├── App.tsx            # Main application
│   └── main.tsx           # Application entry point
├── index.html
├── package.json
├── vite.config.ts
└── README.md
```

## Contributing

Contributions, bug reports, and feature suggestions are welcome.

1. Fork the repository.
2. Create a branch for your change.
3. Commit your changes.
4. Open a pull request describing the improvement.

## License

No license has been specified yet. Add a `LICENSE` file before distributing or reusing this project under an open-source license.

---

Made with React, TypeScript, and computer vision.
