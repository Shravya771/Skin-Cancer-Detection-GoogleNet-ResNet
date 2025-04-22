# 🔬 Skin Cancer Detection using ResNet and GoogleNet 🔬

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.0%2B-red)](https://pytorch.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](https://opensource.org/licenses/MIT)
[![Dataset](https://img.shields.io/badge/Dataset-HAM10000-orange)](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T)

This repository contains a deep learning project for detecting cancerous vs. non-cancerous skin lesions from medical images using two popular CNN architectures: ResNet and GoogleNet (Inception). The project achieves 80%+ accuracy through hyperparameter optimization.

## 📊 Overview

Skin cancer is one of the most common types of cancer globally. Early detection is crucial for effective treatment. This project leverages deep learning techniques to classify skin lesions as either cancerous or non-cancerous using the HAM10000 dataset.

We compare two state-of-the-art architectures:
- **ResNet**: Known for its skip connections that solve the vanishing gradient problem
- **GoogleNet (Inception)**: Features inception modules with parallel convolutional operations

## 🔢 Dataset

The [HAM10000 dataset](https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/DBW86T) (Human Against Machine with 10000 training images) consists of 10,015 dermatoscopic images of pigmented skin lesions. For our binary classification task, we've grouped these into:
- Cancerous lesions
- Non-cancerous lesions

The dataset includes seven different diagnostic categories:
- Actinic keratoses and intraepithelial carcinoma (akiec)
- Basal cell carcinoma (bcc)
- Benign keratosis-like lesions (bkl)
- Dermatofibroma (df)
- Melanoma (mel)
- Melanocytic nevi (nv)
- Vascular lesions (vasc)

## 🧠 Models

### ResNet
- Residual Neural Network with skip connections
- Addresses the vanishing gradient problem
- Allows for training much deeper networks

### GoogleNet (Inception)
- Features inception modules with parallel convolutions
- Efficient computation with dimension reduction techniques
- Intermediate classifiers for deeper networks

## ✨ Features

- Binary classification of skin lesions (cancerous vs. non-cancerous)
- Implementation of ResNet and GoogleNet architectures
- Hyperparameter optimization for better performance
- Data augmentation to prevent overfitting
- Visualization tools for model evaluation

## 📈 Results

The project achieved 80%+ accuracy on the test set with the following evaluation metrics:

- **Accuracy**: 82.7%
- **Precision**: 83.5%
- **Recall**: 81.9%
- **F1-Score**: 82.7%
- **AUC**: 0.89

### Performance Visualization

The repository includes code to generate:
1. Accuracy and loss curves (training vs. validation)
2. Confusion matrices for model evaluation
3. Precision-Recall curves
4. ROC curves

## 🔧 Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/skin-cancer-detection.git
cd skin-cancer-detection
```

2. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Download the HAM10000 dataset:
```bash
python scripts/download_dataset.py
```

## 🔄 Hyperparameter Optimization

We explored six key hyperparameters:

1. **Number of epochs**: 30, 50, 100
2. **Learning rate**: 0.001, 0.0001, 0.00001
3. **Optimizers**: Adam, SGD, RMSprop
4. **Dropout rate**: 0.2, 0.5, 0.7
5. **Batch size**: 16, 32, 64
6. **Number of convolutional layers**: Varies by architecture variant

### Best Hyperparameter Configuration

The best performance was achieved with:

- **Architecture**: ResNet50
- **Learning rate**: 0.0001
- **Optimizer**: Adam
- **Dropout rate**: 0.5
- **Batch size**: 32
- **Epochs**: 50

## 👥 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Created with ❤️ for advancing medical image analysis and early skin cancer detection.
