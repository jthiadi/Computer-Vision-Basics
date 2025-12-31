### Object Detection
This project focuses on **object detection** using RGB images of group-housed swine. The goal is to automatically detect pigs in each image and output bounding boxes for every detected animal.

## 🐖 Task
- Input: 2D RGB image  
- Output: Bounding boxes + confidence scores for each detected pig  
- Evaluation: Detection performance is scored on Kaggle using mAP

## 🧠 Model
a **YOLO-based object detection model** is used
The model performs **single-class detection** (`pig`) by predicting:
- Bounding box location  
- Object confidence score  
- Class label  

## 📤 Output
The final model is used to generate a `submission.csv` file where each row contains:
- Image ID  
- All predicted bounding boxes and class labels for that image  

---

### Long-Tailed Object Detection (Drone Imagery)
This project focuses on **long-tailed object detection** using drone-captured images. The goal is to detect and count real-world objects that appear with highly imbalanced frequencies across classes.

## 🎯 Target Classes
- Car  
- HOV  
- Person  
- Motorcycle  

## 🧠 Model
The project uses **YOLOv8 (Ultralytics)** as the main detection model.  
The dataset is first converted into YOLO format, and the model is trained from scratch (or fine-tuned) to handle long-tailed class distributions.

## 📈 Output
The trained model is used to:
- Perform object detection on test images  
- Generate a `submission.csv` file containing bounding box predictions and class labels, suitable for Kaggle leaderboard submission

---

