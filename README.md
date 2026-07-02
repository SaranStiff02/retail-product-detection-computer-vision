# retail-product-detection-computer-vision

<h1 align="center">🛒 Retail Product Detection using CNN and Transfer Learning</h1>

<p align="center">
  A computer vision deep learning project to classify retail shelf images into background and product categories using CNN and MobileNetV2 transfer learning.
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
  <img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white">
  <img src="https://img.shields.io/badge/Keras-D00000?style=for-the-badge&logo=keras&logoColor=white">
  <img src="https://img.shields.io/badge/CNN-Computer_Vision-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/MobileNetV2-Transfer_Learning-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Jupyter_Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white">
</p>

---

## 📌 Project Overview

This project uses deep learning and computer vision to classify retail product images into different product categories.

The model is trained to identify whether an image belongs to a background class or one of five product classes. This type of image classification system can be used as a prototype for retail shelf monitoring, missing product detection, product availability tracking, and automated inventory checking.

Two deep learning approaches were used:

1. **Custom CNN model**
2. **MobileNetV2 transfer learning model**

The transfer learning model achieved the best performance.

---

## 🎯 Business Problem

Retail stores need to monitor product availability on shelves. Manual shelf checking can be slow, repetitive, and error-prone.

This project demonstrates how computer vision can help automate product recognition and support retail operations by identifying whether expected products are visible in shelf images.

This can support:

* Product availability checking
* Missing product detection
* Shelf monitoring
* Retail inventory support
* Automated visual inspection
* Store operations analytics

---

## 📊 Dataset Information

The dataset contains retail product images organised into class folders.

The dataset used in the notebook is:

```text
MLPR Images
```

The dataset contains:

```text
1938 images
6 classes
```

### Class Labels

| Class      | Description                     |
| ---------- | ------------------------------- |
| Background | Background or non-product image |
| Product_1  | Product category 1              |
| Product_2  | Product category 2              |
| Product_3  | Product category 3              |
| Product_4  | Product category 4              |
| Product_5  | Product category 5              |

### Data Split

| Dataset Split        | Number of Images |
| -------------------- | ---------------: |
| Training             |             1357 |
| Validation / Testing |              581 |

The data was loaded using TensorFlow’s `image_dataset_from_directory()` function with an image size of **224 × 224** and batch size of **32**.

---

## 🛠️ Tools and Libraries Used

| Tool / Library   | Purpose                                  |
| ---------------- | ---------------------------------------- |
| Python           | Deep learning programming                |
| TensorFlow       | Model building and training              |
| Keras            | CNN and transfer learning implementation |
| MobileNetV2      | Pre-trained transfer learning model      |
| NumPy            | Numerical operations                     |
| Pandas           | Data handling                            |
| Matplotlib       | Training and prediction visualization    |
| Seaborn          | Visual analysis support                  |
| Jupyter Notebook | Interactive development environment      |

---

## ✅ Project Workflow

* ✅ Imported required Python libraries
* ✅ Extracted image dataset from zip file
* ✅ Loaded image dataset from directory
* ✅ Resized images to 224 × 224 pixels
* ✅ Split dataset into training and validation sets
* ✅ Applied image preprocessing and augmentation
* ✅ Built a custom CNN model
* ✅ Trained CNN model for product classification
* ✅ Evaluated CNN model accuracy
* ✅ Built MobileNetV2 transfer learning model
* ✅ Applied data augmentation for transfer learning
* ✅ Fine-tuned MobileNetV2 layers
* ✅ Evaluated transfer learning model accuracy
* ✅ Visualized model predictions with predicted and actual labels

---

## 🧠 Image Preprocessing and Augmentation

The project used image augmentation to improve model generalisation.

Augmentation techniques included:

* Rescaling pixel values
* Random horizontal flip
* Random rotation
* Random zoom
* Random contrast
* Width shift
* Height shift
* Shear transformation

These techniques help the model learn product patterns under different viewing conditions.

---

## 🤖 Models Used

### 1. Custom CNN Model

The custom CNN model includes:

* Conv2D layer with 32 filters
* MaxPooling2D layer
* Conv2D layer with 64 filters
* MaxPooling2D layer
* GlobalAveragePooling2D layer
* Dense layer with 128 units
* Dropout layer
* Softmax output layer for 6 classes

The model was compiled using:

```python
model_cnn.compile(
    optimizer="adam",
    loss="categorical_crossentropy",
    metrics=["accuracy"]
)
```

### 2. MobileNetV2 Transfer Learning Model

The transfer learning model uses **MobileNetV2** pre-trained on ImageNet.

The model includes:

* Data augmentation layer
* Rescaling layer for MobileNetV2 input format
* MobileNetV2 base model
* GlobalAveragePooling2D layer
* Dropout layers
* Dense layer with 128 units
* Softmax output layer for 6 classes

The MobileNetV2 base model was first frozen and then fine-tuned by unfreezing selected top layers.

---

## 📊 Model Performance

| Model                         | Accuracy |
| ----------------------------- | -------: |
| Custom CNN                    |   91.22% |
| MobileNetV2 Transfer Learning |   95.35% |

The transfer learning model achieved the highest accuracy.

---

## 🔍 Key Observations

* The dataset contains 1938 images across 6 classes.
* A custom CNN model achieved strong classification performance.
* MobileNetV2 transfer learning improved the accuracy compared with the custom CNN.
* Transfer learning performed better because it uses pre-trained visual features from a large image dataset.
* Data augmentation helped improve model generalisation.
* Prediction visualization helps compare predicted labels with actual labels.

---

## 💼 Business Use Case

This project can be used as a retail computer vision prototype for:

* 🛒 Retail shelf product detection
* 📦 Missing product identification
* 🏪 Store shelf monitoring
* 📊 Inventory visibility support
* 🧾 Automated product availability checking
* 🤖 Computer vision portfolio demonstration
* 📈 Retail operations analytics

The project shows how image classification can support retail automation and product monitoring.

---

## 📁 Folder Structure

```text
retail-product-detection-computer-vision/
│
├── README.md
│   └── retail_product_detection_cnn_transfer_learning.ipynb
│
├── data/
│   └── sample_images/
│
├── images/
│   ├── sample-product-images.png
│   
│
└── docs/
    └── model-insights.md
```

---

## 📂 Project Files

The main notebook is available in the `notebook/` folder:

```text
notebook/retail_product_detection_cnn_transfer_learning.ipynb
```

Sample images can be stored in:

```text
data/sample_images/
```

Dashboard or result screenshots can be stored in:

```text
images/
```

---

## 🎯 What I Learned

* ✅ Loading image datasets using TensorFlow
* ✅ Using `image_dataset_from_directory()`
* ✅ Resizing images for CNN input
* ✅ Applying image augmentation
* ✅ Building a custom CNN model
* ✅ Using Conv2D and MaxPooling2D layers
* ✅ Using GlobalAveragePooling2D and Dropout
* ✅ Building transfer learning models with MobileNetV2
* ✅ Freezing and fine-tuning pre-trained models
* ✅ Evaluating image classification models
* ✅ Visualizing predicted and actual labels
* ✅ Preparing a computer vision project for GitHub portfolio

---

## 🔮 Future Improvements

* 🔲 Add confusion matrix
* 🔲 Add classification report
* 🔲 Add precision, recall, and F1-score per class
* 🔲 Add Grad-CAM visualization
* 🔲 Save the trained model as `.h5` or `.keras`
* 🔲 Add a Streamlit app for image upload prediction
* 🔲 Add more product classes
* 🔲 Improve dataset balance between product categories
* 🔲 Add object detection model such as YOLO for locating products in shelf images
* 🔲 Deploy the model as a retail product recognition demo

---

## ⚠️ Important Notes

This project is created for educational and portfolio purposes.

The current notebook performs image classification, not object detection. It predicts the image class, but it does not locate the exact product position inside the image. For real shelf monitoring, an object detection model such as YOLO, Faster R-CNN, or SSD would be more suitable.

If the dataset is large, upload only sample images to GitHub and mention that the full dataset is not included due to file size.

---

## 👨‍💻 Author

**Saran Kumar Krishnan**

<p>
  <img src="https://img.shields.io/badge/GitHub-SaranStiff02-black?style=for-the-badge&logo=github">
  <img src="https://img.shields.io/badge/Project-Computer_Vision-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge">
</p>
