
# **AI Virtual Mouse Using Hand Tracking** 🖱️🤖  

## **Overview**  
This project implements an **AI-powered virtual mouse** using hand tracking. It uses **OpenCV, MediaPipe, and PyAutoGUI** to detect hand gestures and control the mouse cursor without any physical device.  

## **Features**  
✅ Hand tracking using **MediaPipe**  
✅ Move the mouse cursor with your index finger  
✅ Click with a pinch gesture (index + middle finger close together)  
✅ Smooth movement with interpolation  
✅ Real-time performance with OpenCV  

## **Installation**  

**1️⃣Clone the repository**  
git clone https://github.com/your-username/AIVirtualMouse.git<br>
cd AIVirtualMouse

2️⃣ Install Dependencies
Make sure you have Python (3.x recommended) installed, then run:
pip install opencv-python numpy mediapipe pyautogui

3️⃣ Run the Script
Start the virtual mouse application with:
python AiVirtualMouseProject.py

4️⃣ Allow Camera Access
The script requires webcam access to track your hand gestures.
If the webcam does not start, check your system permissions or try changing the camera index in cv2.VideoCapture(0).

5️⃣ Start Using the Virtual Mouse
Move your index finger to control the cursor.
Bring your index and middle fingers close together to simulate a mouse click.
The performance depends on lighting conditions and webcam quality.


## **How It Works**  

### **1️⃣ Hand Tracking**  
- Captures video from the webcam using **OpenCV**.  
- Uses **MediaPipe** to detect hand landmarks in real-time.  
- Draws hand landmarks on the video feed.  

### **2️⃣ Mouse Movement**  
- The **index finger's position** is mapped to the screen size.  
- Cursor movement is smoothened to avoid jittering using interpolation.  

### **3️⃣ Click Detection**  
- If both **index and middle fingers are up**, the program checks the **distance between them**.  
- If the fingers are close enough (threshold < 40px), a **mouse click** is triggered using **PyAutoGUI**.  

---

## **Customization**  

You can modify different parameters to optimize the experience:  

- **Smoothness of cursor movement**  
  - Increase or decrease `smoothening` in `AiVirtualMouseProject.py`.  
- **Click sensitivity**  
  - Change the threshold value in `findDistance()` to make clicking easier or harder.  
- **Add new gestures**  
  - Modify `fingersUp()` to add additional actions like **scrolling, right-clicking, or drag-and-drop**.  
- **Change camera resolution**  
  - Update `wCam, hCam` in `AiVirtualMouseProject.py`.  

---

## **Troubleshooting**  

### **Common Issues & Fixes**  

🔹 **Camera Not Working?**  
- Make sure the webcam is not being used by another application.  
- Try changing the camera index in `cv2.VideoCapture(0)` (use `1` if you have multiple cameras).  

🔹 **Mouse Movement is Too Fast or Jumpy?**  
- Increase the `smoothening` value to make movement smoother.  
- Ensure there is **enough lighting** for better hand detection.  

🔹 **Clicks Are Not Registering?**  
- Adjust the **distance threshold** in `findDistance()` to make clicking easier or harder.  
- Try moving your hand closer to the camera for better detection.  

---

## **Future Improvements 🚀**  

Here are some planned enhancements:  

✅ **Gesture-based scrolling** (e.g., swipe up/down for page scrolling)  
✅ **Right-click detection** (gesture-based right-click support)  
✅ **Multi-hand support** (control different functions with each hand)  
✅ **Adaptive calibration** (automatic sensitivity adjustment based on hand size/distance)  
✅ **Voice commands integration** (for hybrid control with speech recognition)  

---
 
