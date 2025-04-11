# 🏳️ Religious Classification Using Exploratory Data Analysis and Neural Networks

> Predicting the dominant religion of a country using flag design features and geopolitical attributes with EDA and deep learning.

![Python](https://img.shields.io/badge/python-3.8%2B-blue?logo=python)
![TensorFlow](https://img.shields.io/badge/tensorflow-2.x-orange?logo=tensorflow)
![Neural Networks](https://img.shields.io/badge/Neural%20Networks-enabled-purple)
![CNN](https://img.shields.io/badge/CNN-Convolutional-blueviolet)
![MLP](https://img.shields.io/badge/MLP-Multi--Layer%20Perceptron-lightgrey)


---

## 📚 Overview

This project explores the relationship between a country's **flag design** and its **dominant religion**, leveraging **exploratory data analysis (EDA)** and **neural network models**. Using both **visual (image-based)** and **numerical (CSV-based)** data, we implement and evaluate models like **custom CNNs**, **MobileNetV2**, and **multi-layer perceptrons** to classify religion across countries.

---

## 🧠 Introduction

### 🎯 Research Focus

The core idea is to evaluate **whether visual elements of national flags** can be used to predict a country's **dominant religion**.

### 🧾 Objectives

- Conduct EDA on geopolitical and flag-related features.
- Build ML models that classify religion based on:
  - Flag images (custom CNN, MobileNetV2)
  - Geopolitical numeric data (Multi-layer Neural Network)
- Compare model performance and draw conclusions.

---

## 📊 Dataset

The dataset includes **177 countries** with **30+ features**, such as:

- **Geopolitical attributes**: continent, population, area, language, religion
- **Flag design features**: number of colors, dominant color, presence of symbols (crosses, stars, crescents, suns, circles)

### 🖼️ Flag Images

A custom dataset of flag images (from 1986) is compiled and aligned with the CSV metadata.

---

## 🧪 Methodology

### 1. Data Cleaning

- Removed irrelevant files and images
- Mapped image names to countries
- Standardized categories and labels

### 2. Exploratory Data Analysis (EDA)

- Distribution of colors, symbols, and religion types
- Correlation matrices (e.g., between symbols and religion)
- Comparative visualizations across continents and religions

### 3. Model Development

| Model Type | Input | Description |
|------------|-------|-------------|
| **Custom CNN** | Flag Images | Designed from scratch to classify religion |
| **MobileNetV2** | Flag Images | Pre-trained model adapted to our dataset |
| **MLP** | CSV Data | Neural network trained on numerical features |

---

## 📈 Results

### 🔍 EDA Insights

- **Red** and **white** are the most frequent flag colors globally.
- **Christian** countries often feature **crosses** on their flags.
- Flags of **Muslim-majority** countries frequently feature **green** and **crescent symbols**.

### 🤖 Model Performance

| Model | Accuracy (Global) | Accuracy (Africa) |
|-------|------------------|-------------------|
| **Custom CNN** | 50% | **80%** |
| **MobileNetV2** | 20% | 20% |
| **MLP (CSV)** | 56% (peak) | - |

> ⚠️ **Note:** Low accuracy is due to limited dataset size and visual diversity among flags.

---

## 📌 Conclusion & Future Work

### 🔎 Key Takeaways

- Flag design **does show some correlation** with religion, but it's not conclusive.
- Dividing countries by **region** improves model accuracy.
- Complex geopolitical and historical factors limit prediction reliability.

### 🚀 Future Improvements

- Use **higher-resolution** and **modern flag images**
- Expand dataset for better generalization
- Add **contextual geopolitical data**
- Fine-tune and ensemble models

---

## 🛠️ Setup & Usage

### 📋 Prerequisites

- Python 3.8+
- Libraries:  
  `tensorflow`, `keras`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

---

### ▶️ Running the Project

You have two options for running the project:

#### ✅ Option 1: Run on **Google Colab**  
- Simply upload the main code file and the `datasets/` folder (containing `flag_images/` and `flags_csv/`) to your Colab session.  
- Then, run the cells in the provided notebooks for **EDA** and **data preprocessing**.  
- You can also train models (CNN, MobileNetV2, MLP) by running the corresponding code cells in the notebook.

#### 💻 Option 2: Run Locally  
- Clone the GitHub repository:
  ```bash
  git clone https://github.com/your-username/religious-classification.git
  cd religious-classification
  ```
- Make sure your environment is set up (e.g., with `requirements.txt` or using `conda`/`venv`).
- Run the notebook for EDA and preprocessing.
- For **model training**, run the script cells in the provided notebooks.

---

### 📂 Dataset Preparation

- Place your datasets in the following structure:

```
religious-classification/
├── datasets/
│   ├── flag_images/
│   └── flags_csv/


```


## 📚 References

- [UCI Flags Dataset](https://archive.ics.uci.edu/ml/datasets/Flags)
- Flag Images: Flaglog 1986
- TensorFlow & Keras Documentation
- [MobileNetV2 Paper](https://arxiv.org/abs/1801.04381)