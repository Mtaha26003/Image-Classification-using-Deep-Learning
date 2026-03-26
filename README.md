# 🧠 Image Classification using Deep Learning

This project implements an **Image Classification system using Convolutional Neural Networks (CNN)** built with **TensorFlow and Keras**.  
The model classifies images into different categories and assigns them to a **specific conveyor belt for automated sorting**.

The project demonstrates the full **deep learning pipeline**, including dataset preparation, model training, evaluation, and prediction.

---

## 📌 Project Features

- Image classification using **CNN**
- Dataset preprocessing and loading
- Model training using **TensorFlow/Keras**
- Prediction on new images
- Conveyor belt assignment based on predicted class
- Implemented in **Python using Google Colab / Jupyter Notebook**

---

## 🛠️ Technologies Used

- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- Google Colab / Jupyter Notebook
- Deep Learning (CNN)

---

## 📂 Dataset Structure

The dataset is stored as a ZIP file (`DLimages.zip`) and contains three classes.

```
DLimages/
│
├── black/
│   ├── img1.jpg
│   ├── img2.jpg
│
├── color/
│   ├── img1.jpg
│   ├── img2.jpg
│
├── transparent/
│   ├── img1.jpg
│   ├── img2.jpg
```

Each folder represents a **class label used for training the model**.

---

## 🧠 Model Architecture

The CNN model consists of the following layers:

- Conv2D (32 filters) + ReLU  
- MaxPooling2D  
- Conv2D (64 filters) + ReLU  
- MaxPooling2D  
- Conv2D (128 filters) + ReLU  
- MaxPooling2D  
- Flatten Layer  
- Dense Layer (128 units)  
- Output Layer (Softmax)

**Input Image Size:**  
`224 × 224 × 3`

---

## 🚀 Training the Model

The dataset is split into:

- **80% Training Data**
- **20% Validation Data**

Example training code:

```python
model.fit(train_data, validation_data=validation_data, epochs=5)
```

---

## 📊 Model Evaluation

After training, the model performance is evaluated using validation accuracy and loss.

Example output:

```
Validation Accuracy: 88%
Validation Loss: 0.42
```

---

## 🔍 Prediction System

The trained model can predict the class of a new image.

Each class is mapped to a **conveyor belt**:

| Class | Conveyor Belt |
|------|---------------|
| Black | A |
| Color | B |
| Transparent | C |

Example mapping:

```python
conveyor_belt_map = {
    "black": "A",
    "color": "B",
    "transparent": "C"
}
```

Example output:

```
Predicted Class: Color
Assigned Conveyor Belt: B
```

---

## 💾 Model Saving

The trained model is saved as:

```
imgcolor_classification_model.h5
```

Load the model later using:

```python
from tensorflow.keras.models import load_model
model = load_model("imgcolor_classification_model.h5")
```

---

## ▶️ How to Run the Project

1. Clone the repository

```
git clone https://github.com/your-username/your-repository-name.git
```

2. Install required libraries

```
pip install tensorflow numpy matplotlib
```

3. Open the notebook

```
Image Classification using Deep learning.ipynb
```

4. Upload the dataset (`DLimages.zip`) and run all cells.

---

## 📈 Future Improvements

- Apply **Transfer Learning (ResNet, MobileNet, EfficientNet)**
- Increase dataset size
- Add **data augmentation**
- Build a **web interface for predictions**
- Deploy the model using **Flask or FastAPI**

---

## 👨‍💻 Author

Taha Khan  

Deep Learning / Computer Vision Enthusiast

---

⭐ If you find this project useful, consider **starring the repository**.
