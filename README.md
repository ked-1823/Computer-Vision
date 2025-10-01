# **Real-Time Face, Eye & Smile Detection with Screenshot Capture**

## **Overview**
This project detects **faces, eyes, and smiles in real-time** using a webcam feed.  
It uses **OpenCV's Haar cascade classifiers** to detect facial features, overlay bounding boxes, display detection messages, and capture screenshots when the user presses a key.  

It demonstrates **grayscale conversion, region-of-interest extraction, dynamic overlays, and keyboard interaction** in a practical, real-time computer vision application.

---

## **Features**
- **Face Detection:** Highlights detected faces with **green rectangles**.  
- **Eye Detection:** Highlights detected eyes inside each face with **blue rectangles**.  
- **Smile Detection:** Highlights detected smiles inside each face with **red rectangles**.  
- **Text Overlay:** Displays **"face detected"**, **"eye detected"**, and **"smile detected"** above detections.  
- **Screenshot Capture:** Press **`s`** to save the current frame with all detections.  
- **Quit Program:** Press **`q`** to exit the webcam feed safely.  

---

## **How It Works**
1. **Load Haar Cascade Classifiers**  
   Pretrained XML classifiers for **faces, eyes, and smiles** are loaded. Haar cascades work on **grayscale images**, so frames are converted before detection.

2. **Capture Webcam Frames**  
   The program continuously reads frames from the webcam to create a **real-time video feed**.

3. **Convert Frames to Grayscale**  
   Each frame is converted to grayscale to match the format expected by Haar cascades.

4. **Detect Faces**  
   The face classifier scans the grayscale frame and identifies **rectangular regions** where faces are detected.  
   - Green rectangles are drawn around faces.  
   - **"face detected"** text is displayed above each face.

5. **Detect Eyes Within Each Face**  
   For each detected face, a **Region of Interest (ROI)** is defined, and the eye classifier detects eyes within that ROI.  
   - Blue rectangles are drawn around eyes.  
   - **"eye detected"** text is displayed above the face.

6. **Detect Smiles Within Each Face**  
   The smile classifier scans the same ROI to detect smiles.  
   - Red rectangles are drawn around smiles.  
   - **"smile detected"** text is displayed slightly above or near the face.

7. **Keyboard Interaction**  
   - Press **`s`** → saves the current frame as a screenshot.  
   - Press **`q`** → exits the program gracefully and releases the webcam.

8. **Save Screenshots**  
   Screenshots are saved in the **current working directory** with sequential filenames, and the absolute path is printed for reference.

---

## **How to Use**
1. Run the notebook or script on a computer with a webcam.  
2. Position your face in front of the camera.  
3. Green rectangles appear around faces, blue rectangles around eyes, and red rectangles around smiles.  
4. Press **`s`** to save a screenshot.  
5. Press **`q`** to quit the program.

---

## **Learning Outcomes**
- Understand **Haar cascade classifiers** for **faces, eyes, and smiles**.  
- Learn **grayscale conversion** and **ROI extraction** for nested feature detection.  
- Implement **dynamic overlays** for multiple facial features simultaneously.  
- Handle **keyboard interaction** to capture screenshots and control program flow.  
- Gain hands-on experience with **real-time computer vision applications** in OpenCV.
