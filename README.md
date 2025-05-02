# Stress-Detection-Facial-Expressions
 Developed model using CNN, ConvLSTM2D, and temporal attention on FER-2013 facial video sequences.

This project explores the use of deep learning to detect **human stress levels** from facial expressions — not just from a single image, but by analyzing **sequences of frames**. Our goal is to help build smarter mental health tools by teaching machines to "read between the frames."

---

##  Approaches Implemented

### 🔬 **Approach 1: Temporal Attention Model**
A powerful, interpretable model that:
- Uses **MobileNetV2** to extract features from each frame
- Captures **temporal patterns** using `ConvLSTM2D`
- Applies a **custom attention mechanism** to focus on important frames
- Outputs both a **prediction** and **attention scores** for interpretability

> Great for video-based analysis, behavior monitoring, and detailed insight into *why* a person may appear stressed.

---

###  **Approach 2: Image-Level Baseline Model**
A simpler but effective baseline:
- Classifies stress from **single facial images**
- Uses either a custom CNN or pretrained MobileNetV2
- Fast, lightweight, and deployable in real-time applications

> Best for static images, mobile apps, or edge devices.

---

##  Dataset Used

Based on the [FER2013](https://www.kaggle.com/datasets/msambare/fer2013) dataset:
- Originally a 7-class emotion dataset
- Relabeled into 2 binary classes:
  - **Stress** = angry, fear, disgust, sad
  - **Non-Stress** = happy, neutral, surprise

We then created:
- Sequences of 10 consecutive frames for Approach 1
- Individual frame samples for Approach 2

---

## Key Features

- Custom **temporal attention layer** for interpretability
- Support for both image and sequence-based stress detection
- Pretrained MobileNetV2 backbone
- Attention visualization and ZIP-based evaluation
- Clean modular code (`temporal_model.py`) ready for reuse

---

## 💡 How to Use

1. **Clone this repo:**
   ```bash
   git clone https://github.com/your-username/stress-detection.git
   cd stress-detection
