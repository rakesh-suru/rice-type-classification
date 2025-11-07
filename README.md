# 🌾 Rice Type Classification (PyTorch + Streamlit)

This project classifies rice grains into different types based on grain morphology features such as area, perimeter, aspect ratio, eccentricity, etc. A neural network model is trained using PyTorch and deployed as an interactive web app using Streamlit.

---

## 🚀 Demo
Run the app locally:
```bash
streamlit run app.py
```

The UI allows:
- **Single prediction** using input sliders/number fields.
- **Batch prediction** by uploading a CSV file.

---

## 📁 Project Structure
```
Rice Type Classification/
│
├── app.py                     # Streamlit UI
├── model_state_dict.pth       # Trained PyTorch model weights (state_dict)
├── rice_classifier_pytorch.ipynb  # Model training notebook
├── riceClassification.xlsx    # Dataset
└── README.md
```

---

## 🧠 Model Details
- Model Type: **Fully Connected Neural Network (Tabular MLP)**
- Framework: **PyTorch**
- Input Features:  
  ```
  Area
  MajorAxisLength
  MinorAxisLength
  Eccentricity
  ConvexArea
  EquivDiameter
  Extent
  Perimeter
  Roundness
  AspectRation
  ```
- Output: Class label corresponding to rice type.

---

## 🏋️ Training Overview
The model was trained on a labeled rice dataset with morphological features extracted from grain images. The model learns to discriminate rice varieties based on shape and size characteristics.

If you're using the notebook:
```bash
pip install torch pandas scikit-learn matplotlib
jupyter notebook
```

---

## 🖥️ Running the Streamlit App
### 1. Install dependencies:
```bash
pip install streamlit torch pandas numpy
```

### 2. Run:
```bash
streamlit run app.py
```

---

## 🔢 Batch Prediction Format
Upload a CSV containing **only the feature columns** listed above (no label column required).
Example:
```csv
Area,MajorAxisLength,MinorAxisLength,Eccentricity,ConvexArea,EquivDiameter,Extent,Perimeter,Roundness,AspectRation
5000,150,60,0.92,5400,90,0.59,310,0.74,2.51
...
```

---

## 🏆 Results
- Achieved high classification accuracy after training.
- Smooth user interaction through Streamlit UI.

---

## 🤝 Contributing
Feel free to submit issues or pull requests to improve this project!

---

## 📜 License
This project is released under the MIT License.
