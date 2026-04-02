# 🚜 Offroad Scene Segmentation using DINOv2

## 📌 Project Overview

This project focuses on **off-road scene understanding** using **semantic segmentation**.
The goal is to classify each pixel in an image into meaningful categories such as trees, rocks, sky, grass, etc.

We use a **DINOv2 pretrained backbone** to extract strong visual features and train a **segmentation head** on top of it.

---

## 🎯 Problem Statement

Given an off-road image, the model should:

* Identify different objects in the scene
* Assign a class label to **each pixel** (pixel-level classification)

---

## 🧠 Approach

1. **Input Image**

   * RGB image of off-road terrain

2. **Feature Extraction (DINOv2)**

   * Pretrained Vision Transformer
   * Extracts high-level features from images

3. **Segmentation Head**

   * Custom ConvNeXt-style CNN
   * Converts features into pixel-wise predictions

4. **Output**

   * Segmentation mask with class labels (0–9)

---

## 🏷️ Classes

| Class ID | Label          |
| -------- | -------------- |
| 0        | Background     |
| 1        | Trees          |
| 2        | Lush Bushes    |
| 3        | Dry Grass      |
| 4        | Dry Bushes     |
| 5        | Ground Clutter |
| 6        | Logs           |
| 7        | Rocks          |
| 8        | Landscape      |
| 9        | Sky            |

---

## 🛠️ Technologies Used

* Python
* PyTorch
* DINOv2 (Facebook AI)
* OpenCV
* NumPy
* Matplotlib

---

## 📂 Project Structure

```
Hackthon_project/
│
├── Offroad_Segmentation_Scripts/
│   ├── train_segmentation.py
│   ├── test_segmentation.py
│   ├── segmentation_head.pth
│   └── train_stats/
│
├── Offroad_Segmentation_Training_Dataset/
│   ├── train/
│   └── val/
│
├── Offroad_Segmentation_testImages/
│
└── predictions/
```

---

## 🚀 How to Run

### 1️⃣ Install dependencies

```bash
pip install torch torchvision opencv-python matplotlib tqdm
```

---

### 2️⃣ Train the model

```bash
python train_segmentation.py
```

---

### 3️⃣ Test the model

```bash
python test_segmentation.py
```

---

## 📊 Evaluation Metrics

* **IoU (Intersection over Union)**
* **Dice Score (F1 Score)**
* **Pixel Accuracy**

---

## 📈 Results

* Final IoU: **0.15**
* Dice Score: **0.28**
* Pixel Accuracy: **0.48**

---

## 🔥 Key Features

* Uses **pretrained DINOv2 backbone**
* Performs **pixel-level segmentation**
* Supports **multi-class classification**
* Saves:

  * Predicted masks
  * Colored outputs
  * Comparison images
  * Training graphs

---

## 🚀 Future Improvements

* Increase epochs for better accuracy
* Use data augmentation
* Try advanced segmentation models (UNet, DeepLabV3)
* Fine-tune DINOv2 backbone
* Improve dataset quality

---

## 👩‍💻 Author

Sathvika

---

## 📌 Summary

This project demonstrates how to use **self-supervised vision models (DINOv2)** for **real-world segmentation tasks**, especially in challenging off-road environments.

---
