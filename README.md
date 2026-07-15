# Real-Time Face Detection using OpenCV 📸

This project is a simple application for real-time face detection using a webcam and the OpenCV library in Python. This project was completed as part of Task 1 for a Computer Vision training program.

## 🛠️ Prerequisites
To ensure the project runs smoothly without any conflicts, it is highly recommended to use the following environment setup:
* **Python:** A stable version (e.g., `3.12`).
* **OpenCV:** A stable version (`4.10.0.84` was used for this project).
* **Code Editor:** VS Code or any preferred IDE.

To install the required libraries, run the following command in your terminal:
\`\`\`bash
pip install opencv-python==4.10.0.84
\`\`\`

## 🚀 How to Run
1. Clone this repository or download the `face_detection.py` file.
2. Open your terminal and navigate to the directory containing the file.
3. Run the script using the following command:
\`\`\`bash
python face_detection.py
\`\`\`
4. A window will open displaying your webcam's live feed with a blue bounding box around any detected faces.
5. To safely close the program, click on the video window and press the **'q'** key on your keyboard.

---

## 🧠 Troubleshooting & Journey
During the development of this project, we encountered several common programming errors. We successfully debugged and resolved them to achieve a fully stable environment. Here is a summary of the issues and how we overcame them, which can serve as a helpful reference:

### 1. `pip` or `python` command not recognized
* **Error:** `The term 'pip' is not recognized as the name of a cmdlet...`
* **Cause:** The Python path was not added to the Windows environment variables (PATH) during installation.
* **Solution:** Reinstalled Python from the official website, ensuring the **`Add python.exe to PATH`** checkbox was ticked at the bottom of the installer. 

### 2. Numpy/OpenCV Incompatibility and C++ Build Failures
* **Error:** `numpy.core.multiarray failed to import` and `metadata-generation-failed` during installation.
* **Cause:** Using an experimental/pre-release Python version (`Python 3.14`) which lacked pre-built wheels for the libraries. This forced the system to attempt building them from scratch using C++, resulting in a failure.
* **Solution:** Switched the Python interpreter in VS Code to a stable version **(Python 3.12)** and forced the installation specifically in that environment using:
\`\`\`bash
py -3.12 -m pip install opencv-python
\`\`\`

### 3. Missing `CascadeClassifier` Attribute
* **Error:** `AttributeError: module 'cv2' has no attribute 'CascadeClassifier'`
* **Cause:** The package manager automatically downloaded an unstable pre-release version of OpenCV (v5.0.0.93) where this tool was temporarily modified or missing.
* **Solution:** Uninstalled the unstable pre-release version and explicitly installed a reliable, stable version (`4.10.0.84`):
\`\`\`bash
py -3.12 -m pip uninstall opencv-python -y
py -3.12 -m pip install opencv-python==4.10.0.84
\`\`\`

---
**The project was successfully completed after thorough debugging to ensure a 100% stable runtime environment. 💪**
