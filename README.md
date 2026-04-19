# ColabDoom

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1OQ29Bw7lKbrbz0W8Shj3JgpKHRidRWOT?usp=sharing)

Run the classic DOOM engine inside Google Colab using a headless virtual display pipeline and access it directly through a web browser.

![DOOM Cover](https://upload.wikimedia.org/wikipedia/en/5/57/Doom_cover_art.jpg)

## Overview

ColabDoom demonstrates how a graphical application can be executed in a headless cloud environment using a virtual framebuffer and streamed to a browser via a VNC-based pipeline.

This project focuses on system architecture and reproducibility rather than performance.

---

## Architecture

1. PrBoom+ (DOOM Engine)
2. Xvfb (Virtual Framebuffer)
3. x11vnc (VNC Server)
4. noVNC + websockify (WebSocket Bridge)
5. Browser (Google Colab iframe)


---

## Tech Stack

- PrBoom+ — DOOM engine source port  
- Freedoom — open-source DOOM-compatible assets  
- Xvfb — virtual display server  
- x11vnc — VNC server  
- noVNC — HTML5 VNC client  
- websockify — WebSocket proxy  

---

## How to Run

1. Open the notebook in Google Colab  
2. Run all cells sequentially  
3. Wait for initialization  
4. DOOM will appear in the embedded browser view  

---

## Controls

| Key | Action |
|-----|--------|
| WASD / Arrow Keys | Movement |
| Ctrl | Fire |
| Space | Interact |
| Shift | Run |
| Alt + Arrow | Strafe |

> Mouse input is disabled due to limitations in browser-based VNC environments.

---

## Configuration

```python
DISPLAY = ":99"
RESOLUTION = "800x600x16"
DOOM_WIDTH = "800"
DOOM_HEIGHT = "600"
```
---

## Limitations
- No audio support
- Mouse input is not reliable
- Single-session environment
- Dependent on Google Colab runtime

---

## Notes
- The framebuffer resolution must match the DOOM rendering resolution
- Lower resolution reduces resource usage
- Higher resolution improves visual clarity

---

## Disclaimer

This project is intended for educational and demonstration purposes only.