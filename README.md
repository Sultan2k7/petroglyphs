# Petroglyph Segmentation using Dual YOLO Inference

This project performs segmentation of petroglyphs from images using two YOLO models. The outputs include binary masks and color-extracted masks, saved for each image.

---

## 🧠 How It Works

1. **Object Detection**: Two YOLO models (`model` and `model2`) detect bounding boxes on each input image.
2. **Segmentation per Box**:
   - Crops each box area from the image.
   - Enhances colors and converts to grayscale.
   - Applies thresholding and connected components to extract petroglyph regions.
3. **Result Assembly**:
   - A binary mask and color-only mask are built for the full image.
4. **Saving Outputs**:
   - All results are saved to two folders: `output_bw/` and `output_color/`.

---

## 📁 Output Structure

masks_output.zip
├── output_bw/
│ ├── image1.png 
│ └── image2.png
├── output_color/
│ ├── image1.png 
│ └── image2.png
## ▶️ Usage

Run the notebook to process all images and save outputs.

## 🔧 Requirements
Python 3.8+
Ultralytics YOLO (pip install ultralytics)
OpenCV
Torchvision
NumPy
Pillow
