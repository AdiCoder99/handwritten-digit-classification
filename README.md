# Handwritten Digit Classification Using an ANN

This project uses a fully connected artificial neural network (ANN) built with TensorFlow/Keras to classify handwritten digits from the [MNIST](http://yann.lecun.com/exdb/mnist/) dataset.

## Project structure

```text
.
├── handwritten_digit_classification_using_ann.ipynb
└── README.md
```

## Approach

The notebook:

1. Loads the MNIST dataset through `keras.datasets.mnist`.
2. Uses 28 × 28 grayscale images as input.
3. Normalizes image pixels by dividing them by 255.
4. Flattens each image into a 784-value vector.
5. Trains a dense neural network with:
   - `Flatten` input layer
   - Dense layer with 128 neurons and ReLU activation
   - Dense layer with 32 neurons and ReLU activation
   - Dense output layer with 10 neurons and softmax activation
6. Compiles the model with the Adam optimizer and sparse categorical cross-entropy loss.
7. Trains for 25 epochs with 20% of the training data used for validation.
8. Predicts test labels and evaluates the results with accuracy.
9. Plots the training and validation loss.

## Results

The recorded notebook run achieved:

- **Test accuracy:** `0.974` (97.4%)
- **Training samples:** 60,000
- **Test samples:** 10,000
- **Trainable parameters:** 104,938

Results may vary slightly when the notebook is rerun because training is not configured with an explicit random seed.

## Requirements

- Python 3
- TensorFlow
- Matplotlib
- scikit-learn
- Jupyter Notebook or Google Colab

Install the required packages with:

```bash
pip install tensorflow matplotlib scikit-learn jupyter
```

## Running the notebook

### Jupyter Notebook

From the project directory, run:

```bash
jupyter notebook
```

Open `handwritten_digit_classification_using_ann.ipynb` and execute the cells from top to bottom. The MNIST dataset is downloaded automatically the first time it is loaded.

### Google Colab

Upload the notebook to [Google Colab](https://colab.research.google.com/) and run each cell in order. The notebook was originally created with Colab metadata and can run there without local dataset preparation.

## Notes

This project is intended for learning and experimentation with image classification and basic neural networks. It does not include a separate inference script or web interface; predictions are currently performed inside the notebook.
