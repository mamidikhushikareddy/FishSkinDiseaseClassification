# Fish Skin Disease Classification

![Python](https://img.shields.io/badge/Python-3.x-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-Keras-orange)
![Model](https://img.shields.io/badge/Model-MobileNetV2-green)
![Accuracy](https://img.shields.io/badge/Accuracy-95%25-brightgreen)
![License](https://img.shields.io/badge/License-MIT-yellow)

A deep-learning based image classification system for identifying **fish skin diseases** using a **custom-built and manually annotated dataset** and transfer learning with **MobileNetV2**.

Unlike projects that rely entirely on existing benchmark datasets, this project involved building and annotating a dataset specifically for the fish skin disease classification problem. The trained model achieved approximately **95% classification accuracy**, demonstrating performance comparable to benchmark datasets used for similar image-classification tasks.

---

## Table of Contents

- [Overview](#overview)
- [Motivation](#motivation)
- [Key Features](#key-features)
- [Custom Dataset](#custom-dataset)
- [Why the Custom Dataset Matters](#why-the-custom-dataset-matters)
- [Methodology](#methodology)
- [Model Architecture](#model-architecture)
- [Project Workflow](#project-workflow)
- [Results](#results)
- [Tech Stack](#tech-stack)
- [Repository Structure](#repository-structure)
- [Getting Started](#getting-started)
- [Limitations](#limitations)
- [Future Improvements](#future-improvements)
- [Disclaimer](#disclaimer)
- [License](#license)
- [Author](#author)

---

## Overview

Fish health plays an important role in aquaculture, where disease outbreaks can affect fish survival, productivity, and overall farm operations.

Manual visual inspection can be time-consuming and may require domain expertise. This project explores the use of **computer vision and deep learning** to automatically classify fish skin diseases from images.

The system uses **MobileNetV2 with transfer learning** to extract visual features and classify fish images into the corresponding disease categories.

A major focus of the project was not only model development, but also **creating and annotating a custom dataset** suitable for the classification problem.

---

## Motivation

Many machine-learning projects use clean and well-established benchmark datasets.

Real-world ML development, however, often starts much earlier:

- collecting relevant data,
- identifying usable images,
- annotating samples,
- organizing classes,
- preprocessing the dataset,
- training the model,
- evaluating performance,
- and making predictions accessible to users.

This project was designed to cover a broader portion of that workflow rather than focusing only on model training.

---

## Key Features

- Built a **custom fish skin disease image dataset**.
- Manually annotated and organized images into disease categories.
- Prepared and preprocessed image data for deep-learning training.
- Applied **transfer learning using MobileNetV2**.
- Built the classifier using **TensorFlow and Keras**.
- Achieved approximately **95% classification accuracy**.
- Obtained performance comparable to benchmark datasets used for similar classification tasks.
- Developed an interactive prediction workflow using **Streamlit**.
- Used **Google Colab** for model development and experimentation.

---

## Custom Dataset

One of the key contributions of this project is the use of a **custom-built and annotated dataset** rather than relying completely on an existing benchmark dataset.

The dataset was developed specifically for the fish skin disease classification problem.

### Dataset Development Process

The workflow included:

1. Collecting fish skin disease images.
2. Reviewing and organizing the collected images.
3. Annotating images according to their corresponding disease categories.
4. Cleaning and preparing the dataset.
5. Structuring the data for model training and evaluation.
6. Applying image preprocessing before passing the images to the neural network.

This allowed the model to be developed using data tailored specifically to the target problem.

### Custom Dataset vs. Benchmark Data

A major objective was to determine whether a model trained using a carefully prepared custom dataset could achieve performance comparable to models trained on established benchmark datasets.

The final MobileNetV2-based classifier achieved approximately **95% accuracy**, indicating that the annotated custom dataset was capable of supporting strong classification performance comparable to benchmark datasets used for similar computer-vision tasks.

> **Note:** The comparison refers to classification performance observed during project evaluation and should not be interpreted as claiming that the datasets are identical in size, distribution, difficulty, or experimental conditions.

---

## Why the Custom Dataset Matters

Machine-learning performance depends not only on the selected algorithm or neural-network architecture, but also heavily on the **quality of the underlying data**.

Building the dataset provided practical exposure to several important ML challenges:

- Data collection
- Image quality assessment
- Manual annotation
- Class organization
- Data preprocessing
- Training-data preparation
- Model evaluation
- Generalization considerations

As a result, this project represents a more complete machine-learning workflow than simply applying a pretrained model to an existing benchmark dataset.

---

## Methodology

The overall approach consists of the following stages.

### 1. Data Collection

Images relevant to fish skin disease classification were collected to create the custom dataset.

### 2. Data Annotation

The collected images were manually annotated and assigned to their corresponding disease categories.

### 3. Data Preparation

The annotated images were cleaned, organized, and prepared in a format suitable for model training.

### 4. Image Preprocessing

Images were transformed into the format required by the neural network before training.

Preprocessing helps maintain consistent input dimensions and ensures compatibility with the pretrained MobileNetV2 architecture.

### 5. Transfer Learning

Instead of training a deep convolutional neural network completely from scratch, the project uses **MobileNetV2** as the base architecture.

Transfer learning allows the model to benefit from visual features learned from a large image dataset and adapt them to the fish skin disease classification problem.

### 6. Model Training

The model was trained on the prepared custom dataset using **TensorFlow/Keras**.

### 7. Model Evaluation

The trained model was evaluated on unseen data to assess its ability to correctly classify fish skin disease images.

### 8. Prediction Interface

A **Streamlit-based interface** was developed to make model predictions easier to interact with through a user-facing application.

---

## Model Architecture

The project uses **MobileNetV2**, a convolutional neural-network architecture designed to provide strong image recognition performance while remaining computationally efficient.

### Why MobileNetV2?

MobileNetV2 was selected because it offers a useful balance between:

- Classification performance
- Computational efficiency
- Model size
- Training requirements
- Inference speed
- Potential deployment on resource-constrained systems

Its relatively lightweight architecture also makes it suitable for future deployment in web, mobile, or edge-based applications.

---

## Project Workflow

```text
                ┌───────────────────────┐
                │   Image Collection    │
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │  Manual Annotation    │
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │ Dataset Organization  │
                │     & Cleaning        │
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │  Image Preprocessing  │
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │      MobileNetV2      │
                │   Transfer Learning   │
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │    Model Training     │
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │   Model Evaluation    │
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │ Disease Classification│
                └───────────┬───────────┘
                            │
                            ▼
                ┌───────────────────────┐
                │ Streamlit Interface   │
                └───────────────────────┘
```

---

## Results

The MobileNetV2-based classification model achieved approximately:

# **95% Classification Accuracy**

on the project evaluation dataset.

The results demonstrate that a carefully collected and annotated custom dataset, combined with transfer learning, can provide strong performance for fish skin disease image classification.

The performance obtained was comparable to benchmark datasets used for similar image-classification tasks.

### Key Result

| Metric | Result |
|---|---:|
| Classification Accuracy | **~95%** |
| Base Architecture | MobileNetV2 |
| Learning Approach | Transfer Learning |
| Dataset | Custom Annotated Dataset |

Accuracy should not, however, be treated as the only indicator of real-world model quality. Additional testing on larger and more diverse external datasets would be required before considering the system suitable for practical diagnostic use.

---

## Tech Stack

| Category | Technology |
|---|---|
| Programming Language | Python |
| Deep Learning | TensorFlow |
| Neural Network API | Keras |
| Architecture | MobileNetV2 |
| ML Approach | Transfer Learning |
| Computer Vision | CNN-based Image Classification |
| Development Environment | Google Colab |
| User Interface | Streamlit |
| Version Control | Git / GitHub |

---

## Repository Structure

```text
FishSkinDiseaseClassification/
│
├── FSDC_final.ipynb
│   └── Model development, training and evaluation notebook
│
├── README.md
│   └── Project documentation
│
└── LICENSE
    └── MIT License
```

The current repository primarily contains the notebook used for model development and experimentation.

---

## Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/mamidikhushikareddy/FishSkinDiseaseClassification.git
```

Navigate into the project directory:

```bash
cd FishSkinDiseaseClassification
```

---

### 2. Open the Notebook

The main project notebook is:

```text
FSDC_final.ipynb
```

It can be opened using:

- Google Colab
- Jupyter Notebook
- JupyterLab

Google Colab is recommended for convenient access to GPU resources.

---

### 3. Install Required Libraries

The project primarily uses Python deep-learning and image-processing libraries.

A typical environment will require packages such as:

```bash
pip install tensorflow numpy pandas matplotlib pillow scikit-learn streamlit
```

Depending on the notebook environment, additional packages may already be available through Google Colab.

---

### 4. Configure the Dataset

The custom dataset is not currently packaged as part of the public repository.

To reproduce training, configure the dataset path in the notebook according to your local or Google Drive directory structure.

A typical classification dataset structure may look like:

```text
dataset/
│
├── class_1/
│   ├── image_001.jpg
│   ├── image_002.jpg
│   └── ...
│
├── class_2/
│   ├── image_001.jpg
│   ├── image_002.jpg
│   └── ...
│
└── ...
```

Use the actual class structure and paths expected by the notebook.

---

### 5. Run the Notebook

Run the notebook cells sequentially to perform:

```text
Dataset Loading
      ↓
Data Preparation
      ↓
Image Preprocessing
      ↓
Model Initialization
      ↓
MobileNetV2 Transfer Learning
      ↓
Training
      ↓
Evaluation
      ↓
Prediction
```

---

## Streamlit Interface

A **Streamlit interface** was developed to provide a simple way of interacting with the trained model.

The application workflow allows a user to provide a fish image and receive the corresponding model prediction.

Conceptually:

```text
Upload Fish Image
        ↓
Image Preprocessing
        ↓
Trained MobileNetV2 Model
        ↓
Disease Prediction
        ↓
Display Result
```

The current public repository primarily contains the model-development notebook. A standalone Streamlit application file can be added to the repository as part of a future update.

---

### Dataset Size and Diversity

The model's ability to generalize depends on the diversity and representativeness of the custom dataset.

### Real-World Conditions

Images captured in real-world aquaculture environments may differ from training data because of:

- Lighting
- Camera quality
- Fish orientation
- Water conditions
- Background noise
- Disease progression
- Image resolution

### Evaluation

The reported accuracy reflects the project's experimental evaluation and does not guarantee equivalent performance on all unseen real-world datasets.

### Diagnostic Use

The model has not been validated as a professional veterinary diagnostic system.

---

## Future Improvements

Several improvements could extend this work further:

- Increase the size and diversity of the custom dataset.
- Expand annotation quality checks.
- Test the model on completely independent external datasets.
- Report class-wise precision, recall, and F1-score.
- Perform additional error analysis using confusion matrices.
- Compare MobileNetV2 against architectures such as EfficientNet and ResNet.
- Add **Grad-CAM** or similar explainability methods to visualize the regions influencing predictions.
- Add confidence scores to model predictions.
- Publish trained model weights.
- Add a standalone Streamlit application to the repository.
- Add a `requirements.txt` file for reproducible environment setup.
- Package the classifier behind a REST API.
- Explore mobile or edge-device deployment for aquaculture environments.

---

## Potential Applications

With further validation and development, computer-vision systems of this type could potentially support:

- Aquaculture monitoring
- Fish health screening
- Early disease identification
- Farm-level decision support
- Automated image-based health assessment
- Research into AI-assisted aquaculture management

These applications would require substantially more real-world validation before practical deployment.

---

## License

This project is licensed under the **MIT License**.

See the [`LICENSE`](LICENSE) file for details.

---

## Author

**Mamidi Khushika Reddy**

GitHub: [@mamidikhushikareddy](https://github.com/mamidikhushikareddy)

Repository: [FishSkinDiseaseClassification](https://github.com/mamidikhushikareddy/FishSkinDiseaseClassification)

---

### If you find this project useful, feel free to explore the repository, experiment with the model, or build upon the work.
