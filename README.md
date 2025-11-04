# Gesture_Classification
Real-Time Gesture Classification using a Vision Transformer (ViT)

This project is a real-time gesture classification system. It uses a custom Vision Transformer (ViT) model, built from scratch in PyTorch, to classify 7 distinct hand gestures captured live from a webcam.

## **Features**

**Real-Time Classification:** Classifies hand gestures live via your webcam.

**7 Gesture Classes:** Trained to recognize **Fist, Palm, Peace, RockOn, ThumbsUp, ThumbsDown, and None (background)**.

**Custom ViT Model:** The Vision Transformer (ViT) is implemented from scratch, including manual patch embedding and multi-head attention, as per the assignment requirements.

## **Model Architecture**
The model is a "Mini-ViT" built with the following hyperparameters (Seed: 91):

hidden_dim: 160 

num_heads: 5 

patch_size: 14

epochs: 11 

## **Dataset**
There is no dataset link for this project (because I've used custome dataset, images of me and my friends).


### **Install Dependencies: Create a requirements.txt file with the following content:**
torch

torchvision

opencv-python-headless

numpy

matplotlib

seaborn

scikit-learn

tqdm

pandas

Then, install them:
pip install -r requirements.txt

## How to Run the Project
This project must be run in sequence.

1. Collect Data
Run the Data Collection notebook (e.g., 1_Data_Collection.ipynb).
Follow the on-screen instructions to press keys and capture ~200-300 images for each of the 7 gesture classes (Fist, Palm, Peace, etc.).
Don't forget to capture plenty of None (background) images.

2. Prepare Data
Run the Validation Split script (e.g., in 2_Data_Preparation.ipynb).
This will automatically move 20% of your training images into the gesture_data/val folder to create a validation set.

3. Train the Model
Run the Model Training notebook (e.g., 3_Training.ipynb).
This step will produce the final vit_gesture_model.pth file.

4. Run the Real-Time Demo
Once you have the vit_gesture_model.pth file, run the Live Demo notebook (e.g., 4_Live_Demo.ipynb).

This will launch your webcam and begin classifying your gestures in real-time.
