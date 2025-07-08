# 🗑️ Garbage Classification with Deep Learning

An AI-powered waste classification system that automatically identifies garbage types such as plastic, metal, paper, etc. This project aims to improve recycling efficiency by enabling smart, real-time waste segregation.

---

## 🌟 What's Inside

- ✅ Deep learning model based on **EfficientNetV2B2** (Transfer Learning)
- ✅ Custom classification layers for trash detection
- ✅ Interactive **Gradio interface** for real-time image predictions
- ✅ Performance evaluation using confusion matrix and heatmaps
- ✅ Clean and extendable codebase

---

## 🔧 Tech Stack

- **Language:** Python
- **Frameworks & Libraries:**
  - TensorFlow / Keras
  - EfficientNetV2B2 (via `tf.keras.applications`)
  - scikit-learn
  - matplotlib + seaborn (for visualization)
  - Gradio (for UI)
  - Jupyter Notebook (for experimentation)

---

## 📂 Dataset

- Images of various waste categories (plastic, metal, paper, etc.)
- Preprocessing:
  - Resized to **124×124 pixels**
  - Split into **80% training** and **20% validation**
  - Loaded using `image_dataset_from_directory()` from TensorFlow

---

## 🧠 How It Works

### 1. Load and Prepare Data
- Resize, batch, shuffle, cache, and prefetch image datasets.
- Apply normalization and augmentation if needed.

### 2. Build the Model
- Use **EfficientNetV2B2** as the base model.
- Add custom classification layers (Dropout + Dense).
- Freeze base model layers initially.

### 3. Train the Model
- **Optimizer:** Adam  
- **Loss Function:** Categorical Crossentropy  
- **Callbacks:** 
  - EarlyStopping (patience = 5)
  - ReduceLROnPlateau (monitor = val_loss)

### 4. Evaluate Performance
- Generate confusion matrix and classification report.
- Visualize model predictions using seaborn heatmaps and matplotlib plots.

### 5. Deploy
- Run a **Gradio interface** to classify uploaded images in real time.

---
