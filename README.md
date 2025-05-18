
# 🤖 Rhinoplasty AI - Front View Nose Modification

Rhinoplasty AI is an AI-powered tool that allows users to modify the **nose shape in a front-view facial image**. It leverages **Stable Diffusion Inpainting** to generate realistic edits and supports various styles like **Small**, **Sharp**, **Round**, **Wide**, and **Natural**.

This is ideal for cosmetic simulation, face editing research, or AI-driven personalization applications.

---

## ✨ Features

- Upload a **front-view face image**
- Automatically detects the nose position using facial landmarks (Dlib)
- Creates a bounding box around the nose area
- Applies **Stable Diffusion Inpainting** to modify nose style
- Supports 5 nose styles:
  - Small
  - Sharp
  - Round
  - Wide
  - Natural
- Simple **Gradio UI** for easy interaction

---

## 🔧 Requirements

Install dependencies:

```bash
pip install gradio diffusers torch torchvision matplotlib dlib opencv-python pillow
```

---

## 📦 Downloads Required

> **You must manually download the following file:**

### 1. Dlib Landmark Predictor (for face and nose detection)

- 📥 Download: [shape_predictor_68_face_landmarks.dat](http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2)
- 🗜️ Unzip and place it in your working directory or Google Drive
- Example path:
  ```
  /content/drive/My Drive/shape_predictor_68_face_landmarks.dat
  ```

---

## 🚀 How to Run

```python
# Load model (already done in your script)
from diffusers import StableDiffusionInpaintPipeline

pipe = StableDiffusionInpaintPipeline.from_pretrained(
    "stabilityai/stable-diffusion-2-inpainting"
).to("cuda" or "cpu")
```

Then run the full script including the `modify_nose_front()` function and `gr.Interface()` for launching the Gradio app.

---

## 🖼️ Example Usage

- Upload your image
- Select a style like "Sharp"
- View the result with a modified nose while the rest of the face remains unchanged

---

## 📌 Notes

- Works best with clear **front-view** facial images
- Does not support **side view** or **non-human** images (yet)
- Multiple faces may cause unexpected edits
- Ensure good lighting and minimal occlusion for best results

---

## 📁 File Structure

```
├── rhinoplasty_ai.py                # Main script
├── shape_predictor_68_face_landmarks.dat  # Pretrained Dlib model
├── requirements.txt                 # Dependencies
└── README.md                        # You're here!
```

---

## 👨‍⚕️ Credits

- [Stable Diffusion by Stability AI](https://github.com/Stability-AI/stablediffusion)
- [Dlib Face Landmarks](http://dlib.net/)
- UI powered by [Gradio](https://gradio.app)

---

## 📬 Contact

For enhancements, multi-angle support, or integrating custom diffusion models, feel free to reach out.


For Both side view and front view code 
# 🧠 Rhinoplasty AI – Nose Style Modification using Stable Diffusion

Rhinoplasty AI is an AI-powered image editing tool that allows users to modify the nose shape in **front-view** or **side-view** face images using **Stable Diffusion Inpainting**. It supports multiple common nose styles and leverages automatic facial landmark or side-profile detection for localized editing.

---

## 🚀 Features

- Modify nose shapes in front or side facial images  
- Automatic detection of nose region using Dlib or OpenCV  
- Uses Stable Diffusion v2 Inpainting model for high-quality edits  
- Supports 10 popular nose styles for each view  
- Web-based interface using Gradio  

---

## 🖥️ Demo

To run the interface:

```bash
python app.py

pip install torch torchvision torchaudio
pip install diffusers transformers
pip install opencv-python dlib
pip install gradio
pip install Pillow


🔍 Model Downloads
The project uses:

Dlib Facial Landmark Model: Download the file and place in the correct path:

shape_predictor_68_face_landmarks.dat

Extract and save to: /content/drive/My Drive/shape_predictor_68_face_landmarks.dat

OpenCV RetinaFace-like Model (for side view):
These are downloaded automatically by the script:

deploy.prototxt

res10_300x300_ssd_iter_140000.caffemodel

🎨 Nose Styles Supported
Front View
Small

Sharp

Round

Wide

Natural

Pointed

Button

Greek

Roman

Snub

Side View
Small

Sharp

Round

Wide

Natural

Pointed

Button

Greek

Roman

Snub

🧪 How to Use
Run the code to launch the Gradio interface.

Upload a face image (either front or side view).

Choose "Front View" or "Side View" based on the image.

Select a desired nose style.

Click on Modify Nose.

View/download the modified image.

🔁 You can try different nose styles on the same image.

📂 Project Structure
graphql
Copy
Edit
rhinoplasty_ai/
│
├── app.py                        # Main Python file with all functionality
├── README.md                     # This documentation file
├── deploy.prototxt               # Auto-downloaded OpenCV config file
├── res10_300x300_ssd_iter_*.caffemodel  # Auto-downloaded OpenCV model file
└── shape_predictor_68_face_landmarks.dat # Pre-trained Dlib file (you must download manually)
📸 Example Results
(Add before and after example images here if available)

🧠 Acknowledgements
Stable Diffusion Inpainting by Stability AI

Dlib Face Landmark Detection

OpenCV Face Detection