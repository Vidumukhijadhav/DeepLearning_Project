# 🥦 Vegetable Image Classification
### Deep Learning-Based Vegetable Image Classification  
**Python • TensorFlow • Flask**

---

## 📋 Project Overview
This deep learning-based web application accurately identifies and categorizes various types of vegetables using Convolutional Neural Networks (CNNs). The system analyzes input images of vegetables and classifies them into 15 predefined categories.

---

## 🎯 Key Features

- **Deep Learning Classification:** CNN model trained on 15,000+ vegetable images  

### 🥕 15 Vegetable Categories
Bean, Bitter Gourd, Bottle Gourd, Brinjal, Broccoli, Cabbage, Capsicum, Carrot, Cauliflower, Cucumber, Papaya, Potato, Pumpkin, Radish, Tomato  

- **Web Interface:** User-friendly Flask-based web application  
- **Real-time Prediction:** Instant classification results  

---

## 🏗️ Technical Architecture

```
User → UI (Upload Image) → Flask App → CNN Model → Prediction → Display Result
```

---

## 🧠 Model Architecture

| Layer | Type | Output Shape | Parameters |
|------|------|-------------|-----------|
| conv2d | Conv2D | (None,150,150,32) | 896 |
| max_pooling2d | MaxPooling2D | (None,75,75,32) | 0 |
| conv2d_1 | Conv2D | (None,75,75,64) | 18,496 |
| max_pooling2d_1 | MaxPooling2D | (None,37,37,64) | 0 |
| flatten | Flatten | (None,87616) | 0 |
| dense | Dense | (None,128) | 11,214,976 |
| dropout | Dropout | (None,128) | 0 |
| dense_1 | Dense | (None,128) | 16,512 |
| dense_2 | Dense | (None,15) | 1,935 |

**Total Parameters:** 11,252,815

---

## 📁 Project Structure

```bash
Greenclassify/
├── flask/
│   ├── app.py
│   ├── vegetable_classification.h5
│   ├── static/
│   │   ├── css/style.css
│   │   ├── js/main.js
│   │   └── img/
│   ├── templates/
│   │   ├── index.html
│   │   ├── prediction.html
│   │   └── logout.html
│   └── uploads/
├── notebooks/
│   └── vegetable_classification_training.ipynb
├── requirements.txt
├── README.md
└── LICENSE
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- Anaconda Navigator (recommended)
- TensorFlow 2.10+

---

### Installation

```bash
git clone https://github.com/your-username/repository-name.git
cd Greenclassify

python -m venv venv
source venv/bin/activate
# Windows
venv\Scripts\activate

pip install -r requirements.txt
```

---

### Dataset Download

```bash
kaggle datasets download -d misrakahmed/vegetable-image-dataset
```

---

### Run the Flask Application

```bash
cd flask
python app.py
```

Open in browser:

```
http://127.0.0.1:5000
```

---

## 📊 Dataset

The model is trained on the Vegetable Image Dataset from Kaggle:

- Training Images: 15,000  
- Validation Images: 3,000  
- Test Images: 3,000  
- Categories: 15 vegetable types  

---

## 🧠 Model Training

Open notebook:

```bash
jupyter notebook notebooks/vegetable_classification_training.ipynb
```

Steps performed:
- Data Collection  
- Data Preprocessing  
- Model Building  
- Model Training  
- Model Evaluation  
- Save Model  

---

## 🌐 Web Application Pages

- **Home Page:** Landing page with project information  
- **Prediction Page:** Upload and classify vegetables  
- **Result Page:** Display classification results  

---

## Usage

1. Navigate to the Prediction page  
2. Click **Choose File**  
3. Click **Submit**  
4. View prediction result  

---

## 📈 Use Cases

- Automated Sorting  
- Quality Control  
- Smart Inventory  

---

## 🤝 Contributing

```bash
git checkout -b feature/AmazingFeature
git commit -m "Add some AmazingFeature"
git push origin feature/AmazingFeature
```

Open Pull Request

---

## 👨‍💻 Author
**Imtiyaj Panhalkar**

---

## 📄 License
This project is licensed under the MIT License — see the LICENSE file for details.
