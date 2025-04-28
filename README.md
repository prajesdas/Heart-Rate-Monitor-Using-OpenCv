
# Heart Rate Monitor Using OpenCV

This project is a **real-time heart rate monitor** that uses **OpenCV**, **cvzone**, and a regular webcam to detect the user's face and estimate their heart rate (BPM - Beats Per Minute) based on subtle skin color changes.

### 🛠 Technologies Used
- Python
- OpenCV
- cvzone
- NumPy
- FFT (Fast Fourier Transform)

---

## 📋 Features
- Real-time face detection
- Non-contact heart rate estimation
- Live BPM plotting
- Smooth UI with overlays using `cvzone`
- FPS display

---

## 📦 Requirements
Install the required Python libraries:
```bash
pip install opencv-python cvzone numpy
```

---

## 📂 How It Works
1. **Face Detection**:  
   Detects the user's face using `cvzone.FaceDetectionModule`.

2. **Region Extraction**:  
   Extracts a region from the face for analysis.

3. **Color Amplification**:  
   Subtle color changes (caused by blood flow) are magnified using **Eulerian Video Magnification** principles.

4. **Fourier Transform**:  
   Applies FFT to extract the dominant frequency from color variations.

5. **Heart Rate Estimation**:  
   Converts the frequency into beats per minute (BPM) and plots it live.

---

## 🚀 How to Run
1. Make sure a webcam is connected.
2. Run the Python script:
   ```bash
   python your_script_name.py
   ```
3. The application will start:
   - It will detect your face.
   - After a few seconds of "Calculating BPM...", your heart rate will appear.
4. Press `q` to quit.

---

## 📸
![Screenshot 2025-04-28 132307](https://github.com/user-attachments/assets/2d35c5cd-4efa-48fa-9020-1313c580606d)

![Screenshot 2025-04-28 132240](https://github.com/user-attachments/assets/cd41f9fc-5988-4efc-bc96-a6496a1a5522)

---

## ⚡ Important Notes
- Ensure good lighting for accurate readings.
- Remain as still as possible during measurement.
- Initial calculation may take a few seconds.
- Works best at **15 FPS** webcam settings.
- **cvzone** is essential for text overlays and plotting.

---
