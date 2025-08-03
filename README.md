# CSE438_PartB_Group1

# Lab Assignment Part B  
## 📊 Image Pre-processing & Baseline Model Benchmarking

---

## 👨‍👩‍👧 Group Members

| Name              | Student ID     |
|-------------------|----------------|
| Samura Rahman     | 2021-3-60-064  |
| Md. Shakil Hossain | 2021-3-60-088  |
| Tasfia Tahsin Annita     | 2021-3-60-031  |
| Kanij Fatema     | 2021-3-60-095  |

---

## 🔗 Google Colab Notebook

👉 [Open Colab Notebook](https://colab.research.google.com/drive/YOUR_SHARED_LINK_HERE)

---

## 📝 Project Description

This project is part of Lab Assignment Part B for CSE 438. The work involved two major phases:

### Part 1: Image Analysis & Pre-processing
We performed comprehensive image enhancement and transformation operations to make the raw data suitable for model learning. The following techniques were applied:

- **Resizing** with aspect ratio preservation  
- **Noise Reduction** using Gaussian and Median filters  
- **Contrast Enhancement** via CLAHE  
- **Color Space Conversion** (RGB → HSV/Lab)  
- **Edge Detection** using Sobel and Canny operators  
- **Training-time Data Augmentation**: Random Flip, Rotate, CutOut, and ColorJitter  

Visual results were demonstrated for each method with before/after comparisons, and the final preprocessing pipeline was integrated into the PyTorch dataloader using Albumentations.

---

### Part 2: Baseline Model Training & Evaluation

We trained **five state-of-the-art image classification models** using consistent hyperparameters and evaluation methods. The models were:

- **MobileNetV3-Large**
- **ConvNeXt-Tiny**
- **EfficientNetV2-Small**
- **DenseNet121**
- **ViT Base/16**

Each model was trained with the same data splits, augmentations, and evaluation settings. We used `timm` for backbone support and applied early stopping and mixed-precision training to optimize training time.

---

## 📊 Model Performance Comparison

| Model             | Test F1 | Params (M) | Inference Time (ms/img) |
|-------------------|--------:|-----------:|-------------------------:|
| **MobileNetV3**       | **0.7637**  |   4.21     |   5.25 ms               |
| ConvNeXt-Tiny     | 0.7199  |  27.82     |   5.17 ms               |
| EfficientNetV2-S  | 0.7024  |  20.19     |   4.18 ms               |
| DenseNet121       | 0.6665  |   6.96     |   4.32 ms               |
| ViT Base/16       | 0.3487  |  85.80     |  12.14 ms               |

---

## 🏆 Best Model Selection

- **Selected Model:** `MobileNetV3-Large`  
- **Why?** It achieved the **highest Test F1-score** (0.7637) while also having the **lowest parameter count** (4.21M), resulting in excellent speed and efficiency.  
- The model is lightweight, fast, and accurate — making it ideal for real-world deployment and further extension in our term project.

---

## 🚀 How to Run Locally

### 1. Clone the project
```bash
git clone https://github.com/yourusername/CSE438_PartB.git
cd CSE438_PartB
