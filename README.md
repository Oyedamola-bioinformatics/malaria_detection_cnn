# Malaria Parasite Detection using Convolutional Neural Network

Automated detection of Plasmodium parasites in thin blood smear images.

## Dataset
- Source: NIH National Library of Medicine
- 27,558 cell images (13,779 Parasitized / 13,779 Uninfected)
- https://data.lhncbc.nlm.nih.gov/public/Malaria/

## Model Architecture
- Input: 128x128x3 RGB
- 3x Conv2D + MaxPooling (16, 32, 64 filters)
- Dense 128 + Sigmoid output
- Total Parameters: 1,629,473

## Performance
- Training Accuracy: 95.99%
- Validation Accuracy: 95.68%
- Loss: binary_crossentropy
- Optimizer: Adam

## Tech Stack
Python, TensorFlow 2.x, Keras, CNN

## Usage
```python
model = tf.keras.models.load_model("malaria_cnn_model.h5")
pred = model.predict(image)
