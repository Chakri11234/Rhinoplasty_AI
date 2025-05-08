
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
