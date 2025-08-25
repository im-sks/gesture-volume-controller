# 🖐️🎚️ Gesture Volume Controller

Control your system’s volume **magically** — just with your hand gestures, captured in real time by your webcam!  
A Python-based project that combines computer vision and hand tracking for touchless, intuitive volume control.

---

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?logo=python" />
  <img src="https://img.shields.io/badge/OpenCV-✓-green?logo=opencv" />
  <img src="https://img.shields.io/badge/MediaPipe-✓-orange?logo=google" />
  <img src="https://img.shields.io/badge/pycaw-✓-purple" />
  <img src="https://img.shields.io/badge/License-MIT-yellow" />
</p>

---

## 🚀 Features

- **Real-time hand tracking** using [MediaPipe](https://google.github.io/mediapipe/)
- **Multi-hand support** (up to 2 hands)
- **Distance-based volume adjustment** (pinch-to-mute, spread-to-max)
- **Visual feedback**: finger distances, volume levels, and indicators
- **Smooth system audio control** via [pycaw](https://github.com/AndreMiras/pycaw)
- **Cross-platform** Python code (volume control for Windows)

---

## 🛠️ Project Structure

<details>
<summary><strong>Click to expand</strong></summary>

```
gesture-volume-controller/
├── hand_tracking.py        # Custom hand tracking class (MediaPipe)
├── volume_controller.py    # Main app: gesture-based volume control
├── README.md               # Project documentation
└── ...                     # Other supporting files/scripts
```
</details>

---

## 📦 Prerequisites

- Python 3.x
- Install dependencies:

```bash
pip install opencv-python mediapipe numpy pycaw comtypes
```

---

## ⚡ Quickstart

1. **Clone the repository**
    ```bash
    git clone https://github.com/yourusername/gesture-volume-controller.git
    cd gesture-volume-controller
    ```

2. **Run the Volume Controller**
    ```bash
    python volume_controller.py
    ```

---

## ✋ How to Use

- **Show your palm** to the webcam.
- **Pinch** your thumb & index finger together = 🔇 *minimum volume*.
- **Spread them apart** = 🔊 *increase volume*.
- **Visual feedback:**
    - <span style="color:blue;">Blue line</span>: Current finger distance
    - <span style="color:green;">Green circle</span>: Minimum volume indicator
    - <span style="color:red;">Red circles</span>: Maximum volume indicator

---

## 🧠 Technical Details

- **Hand Tracking** (`hand_tracking.py`)
    - Uses MediaPipe's hand detection (21 landmarks)
    - Configurable parameters:
        - `mode`: Static/Dynamic
        - `max_hands`: Number of hands to detect
        - `detection_confidence`: Min detection threshold
        - `track_confidence`: Min tracking threshold

- **Volume Controller** (`volume_controller.py`)
    - Maps finger distance to system volume range
    - Uses pycaw for seamless Windows audio control
    - Real-time updates and FPS counter

---

## 🤝 Contributing

1. **Fork** the repo
2. **Create** your feature branch:  
   `git checkout -b feature/AmazingFeature`
3. **Commit** your changes:  
   `git commit -m 'Add some AmazingFeature'`
4. **Push** to the branch:  
   `git push origin feature/AmazingFeature`
5. **Open a Pull Request**

---

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

---

## 🙏 Acknowledgments

- [MediaPipe](https://google.github.io/mediapipe/) for hand tracking
- [PyCaw](https://github.com/AndreMiras/pycaw) for Windows audio control
- [OpenCV](https://opencv.org/) for computer vision tools

---

<p align="center">
  <img src="https://user-images.githubusercontent.com/yourusername/demo-gif.gif" alt="Demo GIF" width="60%" />
  <br/><em>Try it out and control your volume like a wizard! 🧙‍♂️</em>
</p>
