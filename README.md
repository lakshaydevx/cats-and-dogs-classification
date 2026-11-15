# 🐱 Cat and Dog Classification using CNN

## 📌 Project Overview

This project implements a **Convolutional Neural Network (CNN)** using PyTorch to classify images into two categories: Cats and Dogs.

The model learns visual features from images through convolutional layers, ReLU activation and max pooling, followed by fully connected layers for classification.

## 🎯 Project Objectives

- Understand CNN architecture and working.
- Load and preprocess image datasets.
- Build a CNN model from scratch using PyTorch.
- Train the model using backpropagation.
- Evaluate model performance on unseen images.

## 🛠️ Technologies & Libraries Used

- Python
- PyTorch
- Torchvision
- Google Colab
- KaggleHub

### Python Libraries

| Library | Purpose |
|---|---|
| `torch` | Tensor operations and deep learning |
| `torch.nn` | CNN layers, activation functions and loss functions |
| `torchvision` | Image datasets and image processing |
| `torchvision.transforms` | Image resizing and normalization |
| `torch.utils.data` | DataLoader and batch processing |
| `torch.optim` | Model optimization using Adam |
| `kagglehub` | Downloading the Kaggle dataset |

## 📂 Dataset Used

**Dataset Name:** Cat and Dog Classification

**Source:** [Kaggle – Cat and Dog Classification](https://www.kaggle.com/datasets/tongpython/cat-and-dog)

### Dataset Download

The dataset is downloaded directly using KaggleHub.

```python
import kagglehub

path = kagglehub.dataset_download("tongpython/cat-and-dog")
```

### Dataset Categories

- Cats
- Dogs

### Dataset Distribution

| Dataset | Number of Images |
|---|---:|
| Training Set | 8,005 |
| Testing Set | 2,023 |
| Total | 10,028 |

## 🖼️ Data Preprocessing

The following preprocessing steps are applied:

- Images resized to **32 × 32 pixels**.
- Images maintained in RGB format.
- Images converted into PyTorch tensors.
- Pixel values normalized.

### Image Transformation

```python
transform = transforms.Compose([
    transforms.Resize((32, 32)),
    transforms.ToTensor(),
    transforms.Normalize(
        (0.5, 0.5, 0.5),
        (0.5, 0.5, 0.5)
    )
])
```

## 🧠 CNN Architecture

The CNN model is built from scratch using PyTorch.

### Architecture Details

| Layer | Configuration |
|---|---|
| Input Layer | 3 × 32 × 32 (RGB) |
| Convolution Layer 1 | 3 → 32 filters |
| Activation | ReLU |
| Max Pooling | 2 × 2 |
| Convolution Layer 2 | 32 → 64 filters |
| Activation | ReLU |
| Max Pooling | 2 × 2 |
| Convolution Layer 3 | 64 → 128 filters |
| Activation | ReLU |
| Max Pooling | 2 × 2 |
| Flatten | 128 × 4 × 4 |
| Fully Connected Layer | 256 neurons |
| Output Layer | 2 classes (Cat and Dog) |

## ⚙️ Model Training

| Parameter | Value |
|---|---|
| Framework | PyTorch |
| Optimizer | Adam |
| Loss Function | CrossEntropyLoss |
| Batch Size | 32 |
| Image Size | 32 × 32 |
| Training Epochs | 5 |
| Classification Type | Binary Classification |

## 📊 Model Performance

The model achieved the following results during the current training run:

| Metric | Accuracy |
|---|---:|
| Training Accuracy | 80.81% |
| Testing Accuracy | 75.14% |

The training loss decreased from **0.646928** to **0.402424** over five epochs.

## 📁 Project Structure

```text
Cat-Dog-Classification/
│
├── Cat_Dog_Classification.ipynb
├── README.md
└── .gitignore
```

## 🚀 How to Run the Project

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
   ```

2. Open the notebook using Google Colab.

3. Install the required libraries:

   ```bash
   pip install torch torchvision kagglehub
   ```

4. Download the dataset using KaggleHub.

5. Run the notebook cells sequentially.

6. Train and evaluate the CNN model.

## 📚 Learning Outcomes

Through this project, I learned:

- Fundamentals of Convolutional Neural Networks.
- Image preprocessing and transformation.
- Convolution and feature extraction.
- ReLU activation and Max Pooling.
- Flattening and fully connected layers.
- Forward propagation and backpropagation.
- Cross Entropy Loss and Adam optimizer.
- Training and testing model performance.

## 👨‍💻 Author

**Lakshay Mittal**

MCA Student | Aspiring AI/ML Developer

---

⭐ If you find this project useful, consider giving this repository a star!
