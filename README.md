
# 🌍 AI-Assisted Disaster Response Prioritization

## 📌 Project Overview

AI-Assisted Disaster Response Prioritization is a multi-modal machine learning system designed to support emergency response teams by automatically identifying and prioritizing disaster-affected zones. The system combines **satellite image analysis** and **social media text mining** to evaluate physical damage and urgency of distress signals, enabling faster and more informed decision-making during natural disasters such as earthquakes, floods, and storms.

This solution is developed as an interactive **Gradio web application**, where users can upload satellite images and enter disaster-related text to receive a combined priority score indicating the urgency of response required.

➡️ **Repository URL:**
[https://github.com/Huzaima372/ai-disaster-response-prioritization](https://github.com/Huzaima372/ai-disaster-response-prioritization)

---

## 🧠 Key Features

### 📷 Satellite Image Damage Detection
- Uses a convolutional neural network (CNN) model based on ResNet50.
- Predicts the probability of structural damage from satellite imagery.

### 🐦 Tweet Urgency Classification
- Applies NLP techniques with TF-IDF and Logistic Regression.
- Evaluates disaster-related text for urgency signals.

### 🔢 Priority Score Computation
- Combines image damage and tweet urgency:

Priority Score = 0.6 × Damage_Probability + 0.4 × Tweet_Urgency_Probability


- Final classification:
- **High Priority** (score > 0.7)
- **Medium Priority** (0.4 < score ≤ 0.7)
- **Low Priority** (score ≤ 0.4)

### 🖥️ Gradio Demo Application
- Simple and intuitive interactive interface.
- Real-time predictions from both models.
- Suitable for demonstrations and rapid prototyping.

---

## 🚀 Installation

### Clone the Repository
```bash
git clone https://github.com/Huzaima372/ai-disaster-response-prioritization.git
cd ai-disaster-response-prioritization
````

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🎯 Usage Instructions

### Run the Gradio App

```bash
python app.py
```

After running, Gradio will output a local (or public if on Colab) link such as:

```
http://localhost:7860
```

Open the link in your browser to launch the app.

---

## 🖼️ Demo Example

### Sample Inputs

* **Satellite Image**: Upload an image showing visible damage (collapsed buildings, flood zones, etc.)
* **Tweet / Text Input**:
  Example:

  ```
  People trapped under collapsed buildings after earthquake. Urgent rescue teams needed immediately!
  ```

### Expected Output

* **Damage Probability**
* **Tweet Urgency Probability**
* **Computed Priority Score**
* **Priority Classification: High / Medium / Low**

---

## 📁 Repository Contents

```
ai-disaster-response-prioritization/
│
├── app.py                         # Gradio demo application
├── requirements.txt               # Required libraries
├── satellite_damage_model.h5      # Pre-trained damage detection model
├── tweet_urgency_model.pkl        # Trained text classification model
├── tfidf_vectorizer.pkl           # TF-IDF vectorizer for NLP
├── README.md                      # Project documentation
```

---

## 📈 Expected Workflow

1. Upload satellite image for damage analysis
2. Enter disaster-related tweet text
3. System computes:

   * Damage probability
   * Tweet urgency probability
   * Combined priority score
4. Displays priority recommendation

---

## 📌 Dependencies

See `requirements.txt` for exact versions. Key libraries include:

* TensorFlow
* Gradio
* scikit-learn
* numpy
* opencv-python
* pillow

---

## 💡 Future Improvements

This repository serves as a foundation for future enhancements:

* Real-time satellite feed integration
* Geo-tagged tweet processing
* Priority heatmap visualization
* Deployment with Docker or Streamlit sharing

---

## 📄 License

This project is open-source and available under the **MIT License**.

---

## 🙌 Acknowledgements

Thank you to the open-source community and contributors of:

* xView2 dataset (satellite imagery)
* Disaster tweet datasets
* Gradio framework

---

## ⭐ Support

If this project helped you or inspired your work, please ⭐ star the repository!

Contributions and feedback are welcome!
