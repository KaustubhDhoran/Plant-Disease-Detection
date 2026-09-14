# Plant-Disease-Detection
An AI platform using CNN and VGG16 to classify crop leaf diseases—such as early/late blight—with up to 99% accuracy. It features a FastAPI backend and web UI to deliver instant diagnoses, confidence scores, and targeted treatment remedies to help farmers prevent crop loss and cut pesticide misuse.

# 🌿 Plant Disease Detection and Diagnosis Using CNN

An end-to-end deep learning system designed for the automated detection, classification, and diagnosis of plant leaf diseases using Convolutional Neural Networks (CNN) and transfer learning, integrated with a FastAPI backend and web interface.

---

## 📌 Project Overview
Plant diseases cause severe losses in agricultural yield and quality worldwide. Traditional visual inspection by experts is labor-intensive, slow, and prone to error. This project delivers an automated computer vision solution to identify diseases from leaf imagery and instantly suggest targeted chemical and organic remediation measures (supplements, fungicides, and cultural practices).

---

## ✨ Features
- **Deep Learning Architecture:** Custom CNN architecture alongside a fine-tuned VGG16 transfer learning model for feature extraction and classification.
- **High Diagnostic Accuracy:** Up to 99% overall accuracy (custom model achieving ~92.3% and VGG16 reaching up to 99%).
- **Automated Diagnosis & Prescription:** Provides disease name, confidence score, and specific treatment suggestions (e.g., Captan, Acrobat, Parin herbal fungicides).
- **Interactive Web Interface:** Web UI developed with HTML5, CSS, JavaScript, and Bootstrap 5.
- **RESTful API Service:** High-performance backend built using FastAPI.
- **Production Packaging:** Containerized using Docker and Docker Compose.

---

## 🏗️ System Architecture

[Leaf Image Input]
│
▼
[Image Preprocessing] (Resized to 256x256, Normalized to [0, 1])
│
▼
[Data Augmentation] (Rotation, Zooming, Flipping, Shearing)
│
▼
[Feature Extraction & CNN] (VGG16 Backbone / Custom 4-Layer ConvNet)
│
▼
[Classification Head] (Dense Layers + Dropout + Softmax)
│
▼
[FastAPI Backend Engine]
│
▼
[Web UI] (Disease Prediction, Confidence Score, and Treatment Measures)

## 📊 Dataset Specifications
- **Source:** PlantVillage Dataset (Kaggle).
- **Classes Focus:** Early Blight, Late Blight, and Healthy (Potato/Tomato), plus Apple Scab, Grape Black Rot, and Pepper Bacterial Spot.
- **Data Preprocessing:** Bilinear interpolation resizing (256×256), pixel normalization (0 to 1), Gaussian blur/noise filtering.
- **Augmentation:** Random rotations (-40° to +40°), zooming (up to 20%), horizontal/vertical flips, and affine shearing.
- **Data Split:** 70% Training, 15% Validation, 15% Testing.

---

## 🛠️ Technology Stack
- **Languages:** Python 3.x, JavaScript, HTML5, CSS3
- **Frameworks & Libraries:** TensorFlow, Keras, OpenCV, NumPy, Pandas, Scikit-learn, Matplotlib, Pillow
- **Backend API:** FastAPI, Uvicorn
- **Frontend:** Bootstrap 5, Vanilla JavaScript
- **Containerization:** Docker, Docker Compose
- **Development Tools:** VS Code, Jupyter Notebook

---

## ⚙️ Installation & Setup

### 1. Prerequisites
- Python 3.9+ installed
- Git installed
- Recommended: NVIDIA GPU or Intel Core i5/8GB+ RAM

### 2. Clone Repository
```bash
git clone [https://github.com/](https://github.com/)<your-username>/plant-disease-detection-cnn.git
cd plant-disease-detection-cnn

### 3. Create & Activate Virtual Environment
Bash
# Windows
python -m venv venv
venv\Scripts\activate

# Linux / macOS
python3 -m venv venv
source venv/bin/activate

4. Install Dependencies
Bash
pip install --upgrade pip
pip install tensorflow opencv-python fastapi uvicorn numpy pandas matplotlib pillow scikit-learn
🚀 Running the Application
1. Start the FastAPI Server
Bash
uvicorn app:app --reload --host 127.0.0.1 --port 8000
2. Launch the Web Interface
Open your web browser and access the local server:

[http://127.0.0.1:8000](http://127.0.0.1:8000)

Upload a leaf photo and click Predict Now to receive the classification and treatment recommendations.

👥 Authors & Academic Credits
Ayush D. Kadu

Chaitanya G. Bhagat

Kaustubh S. Dhoran

Anjali P. Tambade

Project Guide: Prof. D. S. Kalyankar

Department: Computer Science and Engineering

Institution: Dr. Rajendra Gode Institute of Technology & Research (DRGIT&R), Amravati

Affiliation: Sant Gadge Baba Amravati University (SGBAU) (2024–25)
