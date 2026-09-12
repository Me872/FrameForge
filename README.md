# FrameForge

A fast, browser-based video frame extractor and frame stacker.

FrameForge runs entirely in your browser, so you can extract frames and create stacked images without uploading your videos to a server.

## ✨ Features

- 🎞️ Extract frames from local video files
- 🖱️ Drag-and-drop video importing
- 📁 Standard video file picker
- 📷 Record video directly from your camera
- 🖼️ Export individual frames as PNG
- 📦 Automatically package extracted frames into a ZIP
- 🔢 Multiple extraction rates:
  - Source / 30 FPS fallback
  - 30 FPS
  - 24 FPS
  - 15 FPS
  - 10 FPS
  - 5 FPS
- 🧮 Frame stacking modes:
  - Average
  - Median
  - Lighten
  - Darken
  - Difference
- 📊 Live processing progress
- 📝 Processing log
- 🔍 Preview extracted/stacked results
- 🌙 Glass-style dark interface
- 🚀 No installation required
- 🔒 Video stays on your device

## 🧮 Stacking Modes

### Average

Combines the selected frames by averaging their RGB values.

Useful for:

- Reducing random noise
- Creating motion-blended images
- Long-exposure-style effects

### Median

Uses the median RGB value of each pixel across the selected frames.

Useful for:

- Removing moving objects
- Reducing transient noise
- Creating clean static backgrounds

Median processing is limited to 80 frames to prevent excessive browser memory usage.

### Lighten

Keeps the brightest value from each frame for every pixel.

Useful for:

- Light trails
- Fireworks
- Stars
- Moving lights

### Darken

Keeps the darkest value from each frame.

Useful for:

- Motion analysis
- Dark-object accumulation
- Certain animation and exposure effects

### Difference

Calculates the absolute RGB difference between accumulated frames.

Useful for:

- Motion visualization
- Detecting changes between frames
- Experimental frame effects

## 🌐 Browser Processing

FrameForge does not require a backend.

Everything is processed using browser APIs including:

- HTML5 `<video>`
- Canvas
- Canvas `ImageData`
- `MediaRecorder`
- Blob URLs
- Browser file APIs

Your video is not automatically uploaded anywhere.

## 🚀 Usage

1. Open FrameForge.
2. Drop a video into the upload area or select one with the file picker.
3. Choose an extraction FPS.
4. Select a processing mode.
5. Click **Extract Frames**.
6. Wait for processing to finish.
7. Download the resulting PNG or ZIP.

## 📷 Camera Recording

FrameForge can also record video directly from your camera.

Click:

**Record → allow camera access → Stop**

The resulting WebM recording is automatically loaded into FrameForge for processing.

Camera access generally requires a secure context such as HTTPS or localhost.

## 📦 Output

### Individual frame mode

Selecting:

> None — export individual frames

creates a ZIP containing files such as:

```text
frame_000001.png
frame_000002.png
frame_000003.png
frame_000004.png
...
