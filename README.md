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

> ⚠️ **Note:** The dataset used for this project is **not included in this repository** (to avoid uploading large files).  
> Download it separately from the course Kaggle page.

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

> ⚠️ **Note:** The dataset for this task is also **not included in this repository**.  
> Download it separately from the corresponding Kaggle competition.

---

### Image Generation (Diffusion Model)

This project focuses on **image generation using diffusion-based generative models**.  
The goal is to train a model that can generate realistic images of handwritten digits and evaluate the results using the **Fréchet Inception Distance (FID)**.

> ⚠️ **Note:** The MNIST dataset used for this project is **not included in this repository** to avoid uploading large files.  
> Download the dataset separately as instructed in the assignment.

## 🧠 Model
A **Diffusion Probabilistic Model (DDPM)** is implemented and trained **from scratch** to gradually denoise samples from random noise into meaningful digit images.

The model learns to:
- Add noise to real images during training  
- Reverse the process during sampling  
- Generate new handwritten digit images from pure noise  


## 🧪 Evaluation — FID
The generated images are evaluated using **FID (Fréchet Inception Distance)**:

- A **lower FID score** means the generated images are closer to the real dataset
- FID is computed between:
  - 10,000 generated images
  - The MNIST training dataset

## 📤 Output
The model produces:
- **10,000 generated 28×28 RGB images**
- Saved as `.png` files named:

