# 🌍 Satellite Image Classification using CNN, Grad-CAM, and BLIP

This project uses deep learning techniques to classify satellite images into land use categories using a Convolutional Neural Network (CNN). It also includes interpretability tools like Grad-CAM and a multimodal model (BLIP) for image-text explanations.

---

## 📁 Dataset

We use the **EuroSAT dataset**, which contains over 27,000 satellite images across 10 land use classes:
- AnnualCrop, Forest, HerbaceousVegetation, Highway, Industrial, Pasture, PermanentCrop, Residential, River, SeaLake

The dataset was downloaded manually from:
[https://github.com/phelber/eurosat](https://github.com/phelber/eurosat)

Images are resized to 64x64 and normalized for training.

---

## 🧠 Model

We implemented a basic CNN model using PyTorch with:
- 2 convolutional layers
- ReLU activations
- MaxPooling
- Fully connected output layer with 10 outputs

Training setup:
- Epochs: 5
- Batch sizes: 28 and 64 (tested)
- Optimizer: Adam

---

## 🔍 Interpretability

We used:
- **Grad-CAM** to visualize which image regions influenced the model’s decision.
- **BLIP (Bootstrapped Language Image Pretraining)** to generate text-based descriptions and compare with CNN predictions.

This helped us interpret how well the model understood each class.

---

## 📊 Results

- Achieved high classification accuracy on training and validation sets.
- Grad-CAM helped explain misclassifications visually.
- BLIP provided reasonable captions for most images.


