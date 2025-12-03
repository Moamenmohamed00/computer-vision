# 🤖 Gesture-Based Emoji & Sticker Detection using MediaPipe

## 📌 Overview
This project detects **hand gestures** and **facial expressions** in real-time using a webcam,  
then displays a related **sticker or emoji** (e.g., happy face, salute, shh 🤫, etc.) in a separate window.

It combines **Computer Vision** and **AI-based landmark detection** from **MediaPipe** to create  
an interactive, expressive system that reacts to your movements — like a TikTok filter or AR effect.

---

## 🎯 Features
- ✋ Real-time hand gesture recognition using **MediaPipe Hands**.  
- 😀 Face expression detection using **MediaPipe FaceMesh**.  
- 🎥 Dual-window display:
  - **Camera Feed** – live view with hand/face landmarks.
  - **Sticker Window** – shows the corresponding emoji/sticker.
- 👁️ Recognizes multiple gestures:
  | Gesture | Description | Sticker |
  |----------|--------------|----------|
  | 🤫 `shh` | Finger on lips | STK-20250409-WA0035.webp |
  | 👍 `thumb_up` | Thumb raised | STK-20250409-WA0001.webp |
  | 🙌 `peace` | Both hands raised | STK-20250408-WA0059.webp |
  | 🫡 `shrug` | Hand near head (salute) | STK-20250207-WA0001.webp |
  | 😮 `happy` | Mouth open / tongue visible | STK-20241205-WA0004.webp |
  | ✋ `nope` | Hand in front | STK-20241126-WA0032.webp |
  | 🤦‍♂️ `finger_up` | Two fingers near head | STK-20240725-WA0009.webp |

---

## 🧩 Technologies Used
- **Python 3.10+**
- **OpenCV** – Video capture & display.
- **MediaPipe** – Hand & face landmark detection.
- **ImageIO** – Load and play `.webp` stickers.
- **NumPy** – Image processing utilities.

---

## ⚙️ Installation

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Moamenmohamed00/computer-vision.git
cd computer-vision
2️⃣ Install dependencies
bash
Copy code
pip install opencv-python mediapipe imageio numpy
3️⃣ Run the project
Open proj1.ipynb in Jupyter Notebook or VS Code, then run all cells.

🖼️ Folder Structure
bash
Copy code
computer-vision/
│
├── stickers/                  # Folder containing all .webp stickers
│   ├── STK-20250409-WA0035.webp
│   ├── STK-20250409-WA0001.webp
│   ├── STK-20250408-WA0059.webp
│   ├── STK-20250207-WA0001.webp
│   ├── STK-20241205-WA0004.webp
│   ├── STK-20241126-WA0032.webp
│   └── STK-20240725-WA0009.webp
│
├── proj1.ipynb                # Main notebook file (gesture detection)
└── README.md                  # Project documentation
🧠 How It Works
The camera feed is captured via OpenCV.

MediaPipe detects 21 hand landmarks and 468 facial landmarks.

Based on relative positions:

If certain fingers are up → detects a gesture.

If mouth or tongue visible → detects an expression.

The system shows the matching .webp sticker on a separate window.

🎬 Demo
Here’s an example of the project in action:

Gesture	Output
🫡 Hand near head	
😆 Mouth open	

🧑‍💻 Author
Moamen Mohamed
🎓 Computer Vision & AI Developer
📍 Egypt
🔗 GitHub Profile

💡 Future Enhancements
Add sound effects for each gesture 🎵

Support for animated 3D stickers (GIF or short MP4)

Integrate body pose tracking (MediaPipe Pose)

Export gestures as short clips for social media apps

🏁 License
This project is open-source under the MIT License.
