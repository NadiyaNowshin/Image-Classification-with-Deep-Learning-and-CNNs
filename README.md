# Image Classification with Deep Learning: ANN vs CNN

## Project Overview

This project explores image classification using two different deep learning architectures: a fully connected Artificial Neural Network (ANN) and a Convolutional Neural Network (CNN).

Using either the Fashion-MNIST or CIFAR-10 dataset, the project compares how these architectures learn visual patterns and classify images into different categories.

The main objective is to understand why CNNs are particularly effective for image classification and how architectural differences influence model performance, computational complexity, and generalization.

## Dataset

The project uses one of the following benchmark image classification datasets:

**Option 1: Fashion-MNIST**

- Source: [Fashion-MNIST GitHub Repository](https://github.com/zalandoresearch/fashion-mnist)
- 70,000 grayscale images.
- Image dimensions: 28 × 28 pixels.
- 10 clothing categories.
- 60,000 training images and 10,000 test images.

**Option 2: CIFAR-10**

- Source: [CIFAR-10 Dataset](https://www.cs.toronto.edu/~kriz/cifar.html)
- 60,000 color images.
- Image dimensions: 32 × 32 pixels.
- 10 object and animal categories.
- 50,000 training images and 10,000 test images.

Both datasets are available directly through TensorFlow/Keras.

## Project Objectives

- Load and explore an image classification dataset.
- Visualize sample images and their corresponding labels.
- Normalize image pixel values.
- Prepare training, validation, and test datasets.
- Build a baseline fully connected neural network.
- Develop a CNN with convolutional and pooling layers.
- Apply dropout or batch normalization to reduce overfitting.
- Compare model accuracy and trainable parameters.
- Evaluate classification performance using a confusion matrix.
- Investigate misclassified images and understand model limitations.

## Methodology

### Part A: Data Preparation

Prepare the selected dataset for model training.

Tasks include:
- Load the Fashion-MNIST or CIFAR-10 dataset.
- Display 10 sample images with their labels.
- Normalize pixel values to the range [0, 1].
- Create training, validation, and test splits.
- Inspect image dimensions and class distributions.

### Part B: Baseline Neural Network (ANN)

Build a fully connected neural network as the baseline classification model.

Architecture:

`Flatten → Dense Layers (ReLU) → Softmax`

Tasks include:
- Flatten the input images into one-dimensional feature vectors.
- Add fully connected Dense layers with ReLU activation.
- Use a Softmax output layer for multi-class classification.
- Compile the model using an appropriate optimizer and loss function.
- Train the model using validation data.
- Plot training and validation accuracy and loss.

### Part C: Convolutional Neural Network (CNN)

Develop a CNN to capture spatial patterns and local visual features from images.

The architecture includes:
- At least two Conv2D layers.
- MaxPooling layers.
- Dense classification layers.
- Dropout or Batch Normalization for regularization.
- A Softmax output layer for multi-class classification.

Train the CNN using the same dataset splits as the baseline model and visualize its training and validation accuracy and loss.

### Part D: Model Evaluation and Comparison

Compare the performance of the ANN and CNN using the held-out test dataset.

Evaluation criteria:

| Metric | Description |
|---|---|
| Test Accuracy | Percentage of correctly classified test images |
| Trainable Parameters | Number of parameters updated during training |
| Confusion Matrix | Shows correct and incorrect predictions across classes |

Additional analysis:
- Generate a confusion matrix for the CNN.
- Display five incorrectly classified images.
- Show their actual and predicted labels.
- Discuss possible reasons for classification errors.

### Part E: Reflection and Analysis

Analyze the differences between the two architectures.

Discuss:
- Why CNNs can outperform fully connected networks on image data, even with fewer parameters.
- How convolution and pooling help extract useful visual features.
- Whether either model showed signs of overfitting.
- How dropout and batch normalization influence model performance.
- What additional techniques could improve classification accuracy.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab / Jupyter Notebook

## Project Structure

```text
image-classification-ann-vs-cnn/
│
├── Image_Classification_ANN_CNN.ipynb
└── README.md
```

The notebook contains dataset exploration, preprocessing, model architectures, training experiments, visualizations, and evaluation results.

## How to Run

1. Open the notebook in Google Colab or Jupyter Notebook.
2. Select either Fashion-MNIST or CIFAR-10.
3. Ensure TensorFlow, NumPy, Matplotlib, and Scikit-learn are available.
4. Run the notebook cells in sequence.
5. Train both the baseline ANN and CNN.
6. Review the evaluation metrics and visualizations.

## Results and Findings

Complete this section with the actual results from your experiments.

Include:

| Evaluation Metric | ANN | CNN |
|---|---|---|
| Test Accuracy | 87% | 91% |
| Trainable Parameters | 235,146 | 220,426 |

Also include:
- Training and validation accuracy plots.
- Training and validation loss plots.
- CNN confusion matrix.
- Examples of five misclassified images.
- Observations about model performance and overfitting.

## Conclusion

This project demonstrates the differences between fully connected neural networks and convolutional neural networks for image classification.

By implementing and comparing both architectures, it highlights the importance of spatial feature extraction, parameter sharing, and hierarchical visual learning in CNNs.

The experiments provide practical experience in deep learning model development, performance evaluation, and interpreting classification errors.

## Author

Nadiya Nowshin
