# Fine-Tuning YOLOv5 for Sign Language Detection

This repository contains the fine-tuned YOLOv5 model for detecting sign language gestures. The training process was conducted using a custom dataset, and the model was optimized for real-time sign language recognition.

## 📌 Project Overview

- **Model:** YOLOv5 (cloned from Ultralytics and fine-tuned)
- **Dataset:** Custom sign language dataset
- **Training Pipeline:**
  - Data preprocessing
  - Model training using YOLOv5
  - Validation and performance evaluation
- **Outputs:**
  - Fine-tuned model weights (`best.pt`)
  - Training logs and results (`runs/` folder)
  - Sample inference results

## 🛠️ Setup Instructions

### 1️⃣ Clone the Repository
```bash
 git clone https://github.com/vivek99666/Fine-Tuning-Yolo-v5-for-sign-language-detection.git
 cd Fine-Tuning-Yolo-v5-for-sign-language-detection
```

### 2️⃣ Install Dependencies
Ensure you have Python 3.8+ and install the required dependencies:
```bash
pip install -r yolov5/requirements.txt
```

### 3️⃣ Run Inference on Webcam
To test the model in real time using a webcam:
```bash
python yolov5/detect.py --weights yolov5/runs/train/exp/weights/best.pt --source 0
```

### 4️⃣ Train the Model (Optional)
If you want to retrain the model on a different dataset:
```bash
python yolov5/train.py --img 640 --batch 16 --epochs 50 --data data.yaml --weights yolov5s.pt
```

## 📁 Repository Structure
```
📂 Fine-Tuning-Yolo-v5-for-sign-language-detection
├── 📂 yolov5              # Cloned YOLOv5 model (now modified)
├── 📂 runs                # Training outputs and logs
├── 📂 train               # Training images
├── 📂 valid               # Validation images
├── 📂 test                # Test images
├── data.yaml              # Dataset configuration
├── README.md              # Project documentation
└── requirements.txt       # Required dependencies
```

## 🔥 Results & Performance
- **Mean Average Precision (mAP):** Achieved ~94.75% accuracy on the validation set(mAP@50).
- **Inference Speed:** ~55+ FPS on an RTX 4050.
- **Training Logs:** Available in the `runs/` directory.

## 🚀 Future Improvements
- Expand dataset size for better accuracy.
- Optimize inference for real-time performance.
- Deploy as a web or mobile application.

## 📜 License
This project is open-source and licensed under the MIT License.

## 🤝 Contributions
Contributions are welcome! Feel free to open issues and pull requests.

---

If you have any questions, feel free to reach out. Happy coding! 🚀

