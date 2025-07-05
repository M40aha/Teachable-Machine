# Teachable-Machine
# Converted Keras Model

This repository contains a trained Keras model and its corresponding labels.

## 📄 Files

- `keras_model.h5` — The trained Keras model.
- `labels.txt` — Class labels associated with the model output.

## 🚀 Usage

You can load the model and labels using TensorFlow/Keras to make predictions.

### Example:
```python
from tensorflow.keras.models import load_model

# Load model
model = load_model("keras_model.h5")

# Load labels
with open("labels.txt", "r") as f:
    labels = [line.strip() for line in f]

# Example: Make predictions
import numpy as np
sample_input = np.random.rand(1, height, width, channels)  # Replace with your input shape
predictions = model.predict(sample_input)
predicted_class = labels[np.argmax(predictions)]
print("Predicted class:", predicted_class)
