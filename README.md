
# ⚠️Still making changes to the project



# 🎥 ShakeEye - Webcam Effects in Real Time

Welcome to **ShakeEye**, a Python-based application that applies **real-time visual effects** to your webcam feed! Featuring a clean graphical interface with a neon green theme, ShakeEye allows you to experiment with effects like **"Finger Drawing"**, where you can draw on the screen using hand gestures. The processed feed can be sent to a **virtual webcam**, enabling use in apps like Zoom, OBS, and more.

![Captura de ecrã 2025-05-07 205434](https://github.com/user-attachments/assets/10d068ad-de7c-463c-8914-3d54d5fe7406)


---

## ✨ Features

- **Real-Time Effects**  
  Apply visual effects live, including *Finger Drawing*, which draws green lines based on your finger movements.

- **Graphical Interface (GUI)**  
  Custom-designed UI with a dark background, rounded buttons, and a neon green theme.

- **Virtual Camera Support**  
  Send the processed video stream to a virtual webcam via `pyvirtualcam`.

- **Toggle Filters**  
  Switch between the original and filtered webcam feed with a single button.

- **Startup Sound**  
  Plays a startup theme (`tema.mp3`) when the app launches.

- **Custom UI Design**  
  Centered layout, dark theme, neon accents, and intuitive controls.

---

## 📦 Requirements

- **Python 3.8+**

### Python Libraries:

- `opencv-python` – Video capture and processing  
- `pyvirtualcam` – Virtual camera output  
- `pygame` – Play audio on startup  
- `mediapipe` – Hand gesture detection for "Finger Drawing"  
- `tkinter` – Graphical interface (usually included with Python)

### Optional:

- **OBS Studio** – Required to use `pyvirtualcam` with OBS backend  
- **Audio File**: `tema.mp3` (Place it in the same directory as `main.py`)

---

## ⚙️ Installation

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/ShakeEye.git
cd ShakeEye
```

### 2. Create a Virtual Environment (Optional but Recommended)
```bash
python -m venv venv
# On Unix/macOS
source venv/bin/activate
# On Windows
venv\Scripts\activate
```

### 3. Install the Dependencies
```bash
pip install opencv-python pyvirtualcam pygame mediapipe
```

### 4. Configure OBS Studio (for Virtual Camera Support)

- Download and install [OBS Studio](https://obsproject.com/)
- Open OBS  
- Go to `Tools > VirtualCam`  
- Click `Start`

### 5. Add the Startup Sound

Place `tema.mp3` in the root directory next to `main.py`.  
> *If missing, the program will still run but without sound.*

---

## 🚀 How to Use

### 1. Launch the App
```bash
python main.py
```

### 2. Interact with the Interface

- GUI will open with a dark theme and rounded buttons.
- Select an effect from the dropdown (e.g., *Finger Drawing*).
- Click `Apply Effect` to activate.
- Use the `Disable Filters` button to toggle original webcam view.
- Click `Exit` to close the app.

### 3. Use the Virtual Webcam

- Open an app like Zoom or OBS.
- Choose **"OBS Virtual Camera"** as your video input to see the effects.

### 🎨 *Finger Drawing Effect*

- Select **Finger Drawing** from the dropdown.
- Move your index finger in front of the webcam to draw green lines.
- Lines disappear after 5 seconds.

---

## 📁 Project Structure

```
ShakeEye/
├── main.py                 # Main launcher (GUI, webcam, effects)
├── effects/                # Folder for visual effects (e.g., glitch.py)
├── gui/                    # Folder containing the GUI interface
├── tema.mp3                # Optional startup sound
```

---

## 🛠️ Troubleshooting

### ❌ Error Capturing Frame
- Make sure your webcam is connected and not used by another app.
- Try changing the camera index in `main.py` (e.g., 0 → 1 or 2).

### ❌ Error Starting Virtual Camera
- Ensure OBS VirtualCam is running (`Tools > VirtualCam > Start`)
- Close other apps that may be using the virtual camera.
- Reinstall pyvirtualcam:
  ```bash
  pip uninstall pyvirtualcam
  pip install pyvirtualcam
  ```

### ❌ Error Playing Sound (`tema.mp3`)
- Confirm the file is in the correct folder.
- Test it in a media player.
- Convert to MP3 at 44100 Hz using [Audacity](https://www.audacityteam.org/) if needed.

---

## 👨‍💻 Credits

Developed by **Anonymous-Silva**  
GitHub: [Anonymous-Silva](https://github.com/Anonymous-Silva)  
Made with ❤️ by Anonymous-Silva

---

## 📄 License

This project is licensed under the **MIT License**.  
Feel free to use, modify, and distribute!
