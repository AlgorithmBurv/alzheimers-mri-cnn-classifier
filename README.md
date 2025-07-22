
# 🧠 Alzheimer's MRI CNN Classifier

A convolutional neural network (CNN) built using TensorFlow/Keras to classify MRI brain scans into different stages of Alzheimer’s disease.

---

## 📌 Overview

This project performs multi-class image classification on brain MRI data to detect Alzheimer's stages:

- **Non Demented**
- **Very Mild Demented**
- **Mild Demented**
- **Moderate Demented**

The goal is to assist early diagnosis using deep learning.

---

## 🧾 Dataset

**Source**: [Kaggle - Alzheimer MRI Dataset](https://www.kaggle.com/datasets/sachinkumar413/alzheimer-mri-dataset)

Organized as:

```
alzheimer-mri-dataset/
└── Dataset/
    ├── MildDemented/
    ├── ModerateDemented/
    ├── NonDemented/
    └── VeryMildDemented/
```

Each subfolder contains MRI scan images of patients corresponding to the Alzheimer's stage.

---

## ⚙️ Model Architecture

The CNN architecture includes:

- 3 × Conv2D + MaxPooling layers
- Flatten + Dense layers
- Output: 4 units (Softmax logits)

Input images are resized to **256x256** and normalized using `Rescaling(1./255)`.

---

## 🧪 Training Setup

| Parameter         | Value        |
|------------------|--------------|
| Image Size       | 256x256 px   |
| Batch Size       | 64           |
| Epochs           | 10 (early stop >96% acc) |
| Optimizer        | Adam         |
| Loss Function    | SparseCategoricalCrossentropy |
| Split            | 80% Train, 10% Val, 10% Test |

---

## 📈 Performance

Training and validation metrics are plotted using `matplotlib`.

- **Validation Accuracy**: up to ~96%+
- **Training Time**: ~2–3 minutes (Google Colab GPU)

---

## 🚀 Quick Start

1. Clone the repo:
```bash
git clone https://github.com/your-username/alzheimers-mri-cnn-classifier.git
cd alzheimers-mri-cnn-classifier
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Download dataset from Kaggle and place in:
```
/content/alzheimer-mri-dataset/Dataset
```

4. Open and run `Alzhaimer.ipynb` in Google Colab or Jupyter.

---

## 🧠 Output Labels

| Label | Meaning               |
|-------|------------------------|
| 0     | Non Demented           |
| 1     | Very Mild Demented     |
| 2     | Mild Demented          |
| 3     | Moderate Demented      |

---

## 📦 Dependencies

- TensorFlow
- NumPy
- Matplotlib

Optional:
- OpenDatasets
- Pandas

Install via:
```bash
pip install -r requirements.txt
```

---

## 📜 License

MIT License © 2024 – For academic and research use.

---

## 🙌 Acknowledgements

- [Kaggle Dataset by Sachin Kumar](https://www.kaggle.com/datasets/sachinkumar413/alzheimer-mri-dataset)
- TensorFlow & Keras community
