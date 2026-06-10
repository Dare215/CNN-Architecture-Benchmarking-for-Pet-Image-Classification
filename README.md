# CNN Architecture Benchmarking for Pet Image Classification

## Project Overview

This project benchmarks multiple Convolutional Neural Network (CNN) architectures for binary image classification of cats and dogs. The objective is to compare traditional CNN models with transfer learning architectures to determine which approach provides the highest classification performance while maintaining computational efficiency.

The project evaluates:

* Simple Custom CNN
* VGG16 Transfer Learning
* ResNet50 Transfer Learning

The study investigates model accuracy, loss convergence, feature extraction quality, confusion matrices, and learned feature representations using t-SNE dimensionality reduction.

---

## Business Problem

Image classification is a fundamental computer vision task used across healthcare, security, retail, autonomous systems, and artificial intelligence applications. Selecting the optimal architecture can significantly improve prediction performance while reducing computational costs.

This project demonstrates how deep learning models can automatically learn distinguishing visual characteristics between cats and dogs while comparing different architectural approaches.

---

## Dataset Information

### Dataset

* Cats Images: 349
* Dogs Images: 348
* Total Images: 697

### Data Split

| Class | Train | Validation | Test | Total |
| ----- | ----- | ---------- | ---- | ----- |
| Cats  | 236   | 60         | 53   | 349   |
| Dogs  | 236   | 59         | 53   | 348   |

---

## Project Objectives

* Build a baseline custom CNN classifier
* Implement transfer learning using VGG16
* Implement transfer learning using ResNet50
* Compare model performance across architectures
* Visualize feature representations using t-SNE
* Evaluate classification performance using confusion matrices
* Identify the best-performing architecture

---

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Pandas
* Matplotlib
* Seaborn
* Scikit-Learn
* OpenCV
* PIL
* t-SNE

---

## Repository Structure

```text
CNN-Architecture-Benchmarking-for-Pet-Image-Classification/

├── CNN_Capstone.ipynb
├── cnn_lab_comparison.csv
├── Analysis_Report.pdf
├── Model_Performance_Summary.pdf
├── requirements.txt
├── README.md
│
├── visuals/
│   ├── 01_dataset_validation.png
│   ├── 02_data_augmentation_examples.png
│   ├── 03_simple_cnn_training_results.png
│   ├── 04_simple_cnn_loss_and_confusion_matrix.png
│   ├── 04_confusion_matrix_best_model.png
│   ├── 06_vgg16_training_results.png
│   ├── 07_tsne_feature_visualization.png
│   └── 08_resnet50_tsne_feature_visualization.png
│
└── models/
```

---

# Results & Visualizations

## Dataset Validation

![Dataset Validation](visuals/01_dataset_validation.png)

The dataset validation stage confirms that all cat and dog images were successfully loaded and verified prior to model training.

---

## Data Augmentation Examples

![Data Augmentation Examples](visuals/02_data_augmentation_examples.png)

Image augmentation techniques were applied to improve model generalization and reduce overfitting.

Examples include:

* Rotation
* Zooming
* Horizontal Flipping
* Rescaling
* Translation

---

## Simple CNN Training Results

![Simple CNN Training Results](visuals/03_simple_cnn_training_results.png)

The baseline CNN demonstrated steady improvement during training with increasing validation accuracy over multiple epochs.

Key observations:

* Stable convergence
* Moderate classification performance
* Minimal overfitting
* Strong baseline benchmark

---

## Simple CNN Loss and Convergence

![Simple CNN Loss and Confusion Matrix](visuals/04_simple_cnn_loss_and_confusion_matrix.png)

Training and validation loss curves indicate successful optimization throughout the training process.

Key observations:

* Consistent loss reduction
* Stable convergence
* Acceptable validation performance

---

## Best Model Confusion Matrix

![Confusion Matrix](visuals/04_confusion_matrix_best_model.png)

Confusion matrix analysis shows classification effectiveness across both classes.

### Results

| Actual Class | Predicted Cats | Predicted Dogs |
| ------------ | -------------- | -------------- |
| Cats         | 36             | 17             |
| Dogs         | 15             | 38             |

The model correctly classified the majority of images while maintaining balanced performance between classes.

---

## VGG16 Transfer Learning Results

![VGG16 Training Results](visuals/06_vgg16_training_results.png)

VGG16 significantly improved classification performance through transfer learning.

Advantages observed:

* Faster convergence
* Higher validation accuracy
* Improved feature extraction
* Better generalization performance

---

## Simple CNN Feature Space Visualization

![t-SNE Feature Visualization](visuals/07_tsne_feature_visualization.png)

t-SNE visualization illustrates how the Simple CNN learned internal feature representations.

Observations:

* Partial class separation
* Some overlap between cat and dog clusters
* Demonstrates learned visual features

---

## ResNet50 Feature Space Visualization

![ResNet50 t-SNE Feature Visualization](visuals/08_resnet50_tsne_feature_visualization.png)

ResNet50 generated stronger feature embeddings compared to the baseline CNN.

Observations:

* Improved feature clustering
* Better class discrimination
* Enhanced representation learning

---

# Model Comparison

| Metric             | Simple CNN           | VGG16             | ResNet50          |
| ------------------ | -------------------- | ----------------- | ----------------- |
| Architecture Type  | Custom CNN           | Transfer Learning | Transfer Learning |
| Feature Extraction | Learned from Scratch | Pretrained        | Pretrained        |
| Training Speed     | Moderate             | Fast              | Fast              |
| Generalization     | Moderate             | Strong            | Strong            |
| Accuracy           | Good                 | Better            | Best Overall      |

---

# Key Findings

1. Transfer learning outperformed the custom CNN architecture.

2. VGG16 provided strong performance while requiring fewer training epochs.

3. ResNet50 demonstrated the strongest feature extraction capability.

4. t-SNE visualizations confirmed improved class separation using pretrained networks.

5. Transfer learning remains an effective approach when working with limited image datasets.

---

# Future Improvements

Potential future enhancements include:

* Hyperparameter tuning
* Larger image datasets
* Additional transfer learning architectures
* Data balancing techniques
* Explainable AI using Grad-CAM
* Model deployment through Streamlit
* Real-time inference applications

---

# Author

**Darious Brown**

PhD Candidate – Artificial Intelligence & Machine Learning

GitHub: https://github.com/Dare215

LinkedIn: https://www.linkedin.com/in/dariousbrown

Portfolio: https://dare215.github.io/DariousBrown-Portfolio/

---

## License

This project is intended for educational, research, and portfolio demonstration purposes.
