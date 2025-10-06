# 🎭 Facial Emotion Recognition using CNN + MobileNetV2

This project detects **human emotions in real-time** using a webcam or IP camera feed.  
It uses **TensorFlow**, **OpenCV**, and **MediaPipe** to identify faces and classify emotions such as *Happy, Sad, Angry, Neutral, Fear, Disgust,* and *Surprise*.

---

## 🚀 Features
- 🧠 **Deep Learning (CNN with MobileNetV2)** trained on FER2013 dataset  
- 🎥 **Real-time detection** using webcam or mobile camera (IP Webcam app)  
- 🧩 **MediaPipe Face Detection** for accurate face tracking  
- ⚙️ **TensorFlow model** trained on grayscale images  
- 📊 **Smooth predictions** using averaged probability buffer  

---

## 🗂️ Project Structure
```
Facial-Emotion-Recognition/
├── train_emotion_cnn.py       # Model training script
├── realtime_emotion.py        # Real-time emotion detection
├── fer_MobileNet2.keras       # Saved trained model
├── labels.json                # Emotion label mappings
└── README.md                  # Project documentation
```

---

## ⚙️ Requirements
Install the dependencies using `pip`:

```bash
pip install tensorflow opencv-python mediapipe numpy matplotlib scikit-learn
```

---

## 🧠 Training the Model
To train the model from scratch:
1. Download and prepare the **FER2013 dataset**.
   ```
   dataset/
   ├── train/
   └── test/
   ```
2. Run the training script:
   ```bash
   python train_emotion_cnn.py
   ```
3. This will generate:
   - `fer_MobileNetV2_gray.keras` → trained model  
   - `labels.json` → list of emotion labels  

---

## 🎥 Running Real-Time Emotion Detection
Make sure your trained model and `labels.json` are in the same folder as `realtime_emotion.py`.

Then run:
```bash
python realtime_emotion.py
```

To use your **mobile camera**, replace this line in `realtime_emotion.py`:
```python
url = 0
```
with your IP Webcam URL, for example:
```python
url = "http://192.168.1.5:8080/video"
```

Press **`Q`** to quit the window.

---

## 🧩 Supported Emotions
| Label | Description |
|--------|-------------|
| 😀 Happy | Smiling or joyful |
| 😢 Sad | Unhappy expression |
| 😠 Angry | Frowning or tense |
| 😱 Surprise | Wide eyes or raised brows |
| 😐 Neutral | Relaxed face |
| 😨 Fear | Anxious or tense expression |
| 🤢 Disgust | Nose wrinkled or mouth open |

---

## 📈 Model Summary
The model is based on **MobileNetV2**, modified for grayscale input (48×48).  
It uses data augmentation, dropout, and batch normalization to improve accuracy and reduce overfitting.

---

## 🏆 Results
- Achieved high accuracy on test set (~70–75% depending on training setup).  
- Works in real-time at 20–30 FPS with a CPU or GPU.

---

## 🧑‍💻 Author
**Rugved Ganapuram**  
📧 rugvedg10@gmail.com  
🌐 [GitHub Profile](https://github.com/Rugved-G)

---

## 📜 License
This project is open source under the [MIT License](LICENSE).

---

### ❤️ Acknowledgments
- [TensorFlow](https://www.tensorflow.org/)
- [OpenCV](https://opencv.org/)
- [MediaPipe](https://developers.google.com/mediapipe)
- [FER2013 Dataset](https://www.kaggle.com/datasets/msambare/fer2013)
