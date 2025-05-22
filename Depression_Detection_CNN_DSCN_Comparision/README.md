
# Depression Detection Using CNN and Dual-Scale Convolutional Network (DSCN)

This project demonstrates a deep learning approach to detect emotional expressions using the CK+48 facial expression dataset. Two models—**a standard CNN** and a **Dual-Scale Convolutional Network (DSCN)**—are implemented and compared for performance.

## 📂 Project Structure

- `Code_CNN_and_DSCN_Second_Trial_62_74.ipynb`: Main Jupyter Notebook with code for preprocessing, model building, training, and comparison.
- Dataset: **CK+48** facial expression dataset (must be downloaded separately).
- Models:
  - A standard **Convolutional Neural Network (CNN)**
  - A custom **Dual-Scale Convolution Network (DSCN)** that captures features at multiple scales using both small and large convolutional kernels.

## 📊 Dataset

- **Name**: CK+48 Dataset
- **Format**: Preprocessed 48x48 grayscale images categorized by facial emotion.
- **Labels**: Multiple emotion classes such as Happy, Sad, Angry, Disgust, etc.

## 🚀 Features

- Image preprocessing and normalization
- Data augmentation using `ImageDataGenerator`
- CNN and DSCN model architectures implemented with TensorFlow/Keras
- Model training with validation
- Accuracy comparison using plots

## 🧠 Model Architectures

### CNN (Baseline)
- 2 convolutional layers
- MaxPooling, Flatten, Dense layers
- Dropout regularization

### DSCN (Proposed)
- Dual-branch convolutional paths:
  - Small kernel path (3x3)
  - Large kernel path (7x7)
- Concatenated feature map
- Fully connected layers with dropout

## 📈 Results

| Model | Validation Accuracy (approx) |
|-------|------------------------------|
| CNN   | ~62%                         |
| DSCN  | ~74%                         |

DSCN shows a significant improvement in capturing multi-scale features for emotion detection.

## 🛠️ Requirements

Install required packages with:

```bash
pip install tensorflow numpy matplotlib scikit-learn opencv-python
```

## 🏃‍♂️ How to Run

1. Download the CK+48 dataset and set the correct `DATASET_PATH` in the notebook.
2. Run all cells in `Code_CNN_and_DSCN_Second_Trial_62_74.ipynb`.
3. The notebook will train both models and display a comparison graph.

## 📌 Notes

- Ensure your machine has sufficient memory/GPU if training on full dataset.
- Training time varies with system specs.

## 📬 Contact

For questions or feedback, feel free to open an issue or contact the developer.
