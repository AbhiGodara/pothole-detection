# YOLOv10-Based Pothole Detection System

![YOLOv10 Pothole Detection Banner](https://raw.githubusercontent.com/yourusername/your-repo/main/assets/banner.png)  <!-- Optional image -->

## 🚧 Project Overview
This project presents a complete solution for **pothole detection** using the **YOLOv10 object detection algorithm**. The system was developed and trained in **Google Colab**, and a user-friendly **Streamlit web application** was created for easy interaction. The model identifies potholes in images, video footage, and real-time webcam streams.

## 📦 Dataset
- **Dataset Name:** Pothole Detection Dataset
- **Source:** [Kaggle - rajdalsaniya/pothole-detection-dataset](https://www.kaggle.com/datasets/rajdalsaniya/pothole-detection-dataset)
- **Access Method:** Downloaded using the Kaggle API via a `kaggle.json` authentication file

## 🏗️ Model Training
- **Model Architecture:** YOLOv8l (Ultralytics YOLO)
- **Platform:** Google Colab
- **Base Weights Used:** `yolov8l.pt`
- **Training Duration:** 50 epochs
- **Image Resolution:** 640x640
- **Batch Size:** 8
- **Framework:** Ultralytics YOLO Python package
- **Hyperparameters:** Defined programmatically in Python

### Key Augmentation & Hyperparameters
- Mosaic: 1.0
- Translate: 0.05
- Scale: 0.05
- FlipUD: 0.1
- FlipLR: 0.2
- Mixup: 0.0

### Dataset Configuration YAML
```yaml
train: /content/train/images
val: /content/valid/images
nc: 1
names: ['pothole']

📊 Evaluation Metrics
After training, the model was evaluated on the validation set using Ultralytics' val() method, producing the following metrics:

Metric	Value
Precision	0.988
Recall	0.760
mAP@0.5	0.788
mAP@0.5:0.95	0.383
📷 Visual Validation
Sample predictions on validation images were plotted using Matplotlib, showing bounding boxes and labels over potholes.

🌐 Web Deployment
Interface Framework: Streamlit

Functionalities:

Upload and detect potholes in static images

Upload video files and run frame-by-frame detection

Run live detection using a webcam

Real-Time Features:

Bounding boxes with class labels and confidence scores

Interactive display of results

🚀 How to Run the Project
1. Clone the Repository
bash
Copy
Edit
git clone https://github.com/yourusername/pothole-detection-yolov10.git
cd pothole-detection-yolov10
2. Install Dependencies

pip install -r requirements.txt
3. Launch the Streamlit App

streamlit run deploy.py


📁 Project Structure
graphql
Copy
Edit
├── deploy.py                # Streamlit application
├── pothole_prediction_model.py                 # Trained YOLO model file
├── requirements.txt      # requirements file
├── predicted samples folder          # validation images with prediction
└── README.md



📚 Tech Stack
Python

OpenCV

Streamlit

Ultralytics YOLOv8/YOLOv10

Matplotlib

📝 Author
Abhishek Godara
