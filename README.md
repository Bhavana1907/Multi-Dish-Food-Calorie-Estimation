# 🍽️ Multi-Dish Food Calorie Estimation

A deep learning-based project for **multi-dish food image segmentation and calorie estimation**. The system uses **DeepLabV3+** for food segmentation and is designed to identify food regions from images and estimate their calorie content.

## 📌 Project Overview

Estimating calories from a meal containing multiple food items can be challenging because different dishes may appear together in a single image.

This project explores a computer vision approach that first identifies individual food regions in an image and then uses food information and estimated portion details to support calorie estimation.

The project was developed as a **Minor Project** using the **FoodSeg103** dataset.

## 🎯 Objectives

* Detect and segment multiple food items from a single image.
* Use semantic segmentation to identify individual food regions.
* Estimate food quantity/portion information from the segmented regions.
* Estimate the approximate calorie content of the detected food items.
* Provide an easy-to-use interface for testing food images.

## 🧠 Methodology

The overall workflow is:

```text
Input Food Image
       ↓
Image Preprocessing
       ↓
DeepLabV3+ Segmentation Model
       ↓
Food Item Segmentation
       ↓
Food Identification & Portion Estimation
       ↓
Calorie Database
       ↓
Estimated Calorie Output
```

## 🤖 Model

### DeepLabV3+

**DeepLabV3+** is used for semantic segmentation. It helps identify different regions of an input food image so that individual food items can be analyzed separately.

The model was trained and evaluated using the **FoodSeg103** dataset.

## 📊 Dataset

### FoodSeg103

FoodSeg103 is a food image segmentation dataset containing multiple food categories with pixel-level segmentation annotations.

The dataset is used to train and evaluate the food segmentation component of the project.

## 📈 Results

The DeepLabV3+ model was trained for **20 epochs**.

The recorded Mean Intersection over Union (**Mean IoU**) was:

```text
Mean IoU: 0.18047
```

This result provides a baseline for the current segmentation implementation and can be improved through further model tuning, preprocessing, data augmentation, and training.

## 🛠️ Technologies Used

### Programming

* Python

### Machine Learning / Deep Learning

* DeepLabV3+
* Semantic Segmentation
* Computer Vision

### Libraries / Tools

* PyTorch
* NumPy
* OpenCV
* Matplotlib
* Gradio
* Jupyter Notebook

### Dataset

* FoodSeg103

## 🖥️ User Interface

A simple **Gradio-based interface** is included to allow users to upload food images and interact with the project.

## 📂 Project Structure

```text
Multi-Dish-Food-Calorie-Estimation/
│
├── demo_NB.ipynb
├── project (1).ipynb
├── SVM.ipynb
├── training.ipynb
├── UI.ipynb
└── README.md
```

### Notebook Description

| Notebook            | Purpose                                 |
| ------------------- | --------------------------------------- |
| `training.ipynb`    | Model training and experimentation      |
| `UI.ipynb`          | User interface implementation           |
| `demo_NB.ipynb`     | Demonstration / model usage             |
| `SVM.ipynb`         | SVM-based experimentation               |
| `project (1).ipynb` | Project experimentation and development |

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Bhavana1907/Multi-Dish-Food-Calorie-Estimation.git
```

### 2. Navigate to the project

```bash
cd Multi-Dish-Food-Calorie-Estimation
```

### 3. Install the required dependencies

```bash
pip install torch torchvision numpy opencv-python matplotlib gradio jupyter
```

### 4. Open the notebooks

```bash
jupyter notebook
```

Open the required notebook and follow the cells in sequence.

> **Note:** The complete dataset and trained model files are not included in this repository. They may need to be downloaded or configured separately before reproducing the experiments.

## 🔮 Future Improvements

* Improve segmentation accuracy through better training and augmentation.
* Improve food portion/weight estimation.
* Expand the calorie database with more food categories.
* Improve calorie estimation for mixed dishes.
* Deploy the application as a web application.
* Optimize the model for faster inference.
* Add more robust nutritional information such as carbohydrates, protein, and fats.

## 🌱 Sustainable Development Goals

This project aligns with:

**SDG 3 — Good Health and Well-Being**

Supports awareness of food intake and nutritional information.

**SDG 12 — Responsible Consumption and Production**

Encourages greater awareness of food consumption and portion sizes.

## 👩‍💻 Author

**Bhavana Ponnam**

Computer Science Engineering
GNITS

GitHub: [Bhavana1907](https://github.com/Bhavana1907)

## 📄 License

This project is intended for **academic and educational purposes**.
