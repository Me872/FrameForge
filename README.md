# 🎞️ FrameForge

### Fast, browser-based video frame extraction and frame stacking.

**FrameForge** lets you extract frames from videos, record directly from your camera, and combine frames into powerful stacked images — all directly in your browser.

🎥 **No uploads. No backend. No installation.**

**[🚀 Open FrameForge](https://me872.github.io/FrameForge/)**

---

## ✨ Features

- 🎞️ **Video frame extraction**
- 🖱️ **Drag-and-drop importing**
- 📁 **Video file picker**
- 📷 **Built-in camera recording**
- 🖼️ **PNG frame export**
- 📦 **Automatic ZIP packaging**
- 🧮 **Frame stacking**
- 📊 **Live processing progress**
- 📝 **Detailed processing log**
- 🔍 **Result preview**
- 🌙 **Modern glass-style interface**
- 🚀 **No installation required**
- 🔒 **Local browser processing**
- 🌐 **Works with GitHub Pages**

---

# 🧮 Frame Stacking

FrameForge can process multiple video frames together to create a single composite image.

## Average

Calculates the average RGB value of each pixel across the selected frames.

**Great for:**

- Noise reduction
- Motion blending
- Experimental photography
- Long-exposure-style effects
- Creating smooth composite images

---

## Median

Calculates the median RGB value of each pixel across the selected frames.

**Great for:**

- Removing moving objects
- Reducing transient noise
- Creating clean backgrounds
- Static-scene extraction

> ⚠️ Median stacking is limited to **80 frames** to reduce excessive browser memory usage.

---

## Lighten

For each pixel, FrameForge keeps the brightest RGB values encountered across the frames.

**Great for:**

- ⭐ Stars
- ✨ Light trails
- 🎆 Fireworks
- 💡 Moving lights
- Night photography effects

---

## Darken

For each pixel, FrameForge keeps the darkest RGB values encountered across the frames.

**Great for:**

- Motion analysis
- Dark-object accumulation
- Experimental exposure effects
- Animation analysis

---

## Difference

Calculates absolute RGB differences between accumulated frames.

**Great for:**

- Motion visualization
- Detecting changes
- Comparing frames
- Experimental visual effects

---

# 🎚️ Extraction Rates

FrameForge currently supports:

| FPS | Use |
|---:|---|
| Source | Source-style extraction with a 30 FPS fallback |
| 30 FPS | High frame sampling |
| 24 FPS | Film-style sampling |
| 15 FPS | Medium sampling |
| 10 FPS | Reduced sampling |
| 5 FPS | Fast extraction |

Lower FPS settings can significantly reduce processing time and memory usage.

---

# 📦 Output

## Individual Frames

Select:

> **None — export individual frames**

FrameForge extracts the selected frames as PNG images.

Example:

```text
frame_000001.png
frame_000002.png
frame_000003.png
frame_000004.png
frame_000005.png
...
