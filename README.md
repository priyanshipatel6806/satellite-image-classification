# 🌍 Satellite Image Classification using CNN, Grad-CAM, and BLIP

This project applies deep learning techniques to classify satellite images into land use categories using a Convolutional Neural Network (CNN). It also incorporates interpretability tools like Grad-CAM and a multimodal model (BLIP) for image-text explanations.

---

## 📁 Dataset

We use the **EuroSAT dataset**, which contains over 27,000 satellite images across 10 land use classes:

- AnnualCrop  
- Forest  
- HerbaceousVegetation  
- Highway  
- Industrial  
- Pasture  
- PermanentCrop  
- Residential  
- River  
- SeaLake

The dataset was downloaded manually from:  
👉 [https://github.com/phelber/eurosat](https://github.com/phelber/eurosat)

All images were resized to **64×64** pixels and normalized before training.

---

## 🧠 Model

We implemented a simple CNN model using PyTorch with the following architecture:

- 2 convolutional layers  
- ReLU activation functions  
- MaxPooling layers  
- Fully connected output layer with 10 output classes

**Training configuration:**

- Epochs: 5  
- Batch sizes: 28 and 64 (tested)  
- Optimizer: Adam

---

## 🔍 Interpretability

To make the model interpretable, we used:

- **Grad-CAM**: To visualize which parts of the image influenced the model’s predictions.  
- **BLIP (Bootstrapped Language Image Pretraining)**: To generate textual descriptions of the images and compare them with CNN predictions.

This helped us analyze how well the model "understood" each image class.

---

## 📊 Results

- Achieved high classification accuracy on both training and validation sets  
- Grad-CAM visualizations helped identify reasons behind correct and incorrect predictions  
- BLIP produced meaningful captions for most images, aiding comparison with the model's outputs
