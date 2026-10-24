# Multimodal Skin Disease Diagnosis Using Contrastive Learning

## Overview

This project explores how multimodal deep learning can improve skin disease classification by combining medical images with corresponding clinical descriptions. Using contrastive learning, the model maps visual and textual information into a shared embedding space to learn relationships between skin conditions and their descriptions.

The goal is to improve diagnostic accuracy and explore AI-driven approaches to making dermatological assessment more accessible.

## Key Features

- **Multimodal Learning:** Combines skin disease images and clinical text descriptions.
- **Image Encoding:** Uses a pretrained ResNet50 convolutional neural network (CNN) to extract visual features.
- **Text Encoding:** Uses BERT to generate embeddings from clinical descriptions.
- **Contrastive Learning:** Aligns matching image-text pairs while separating nonmatching pairs in a shared embedding space.
- **Classification:** Combines contrastive and classification losses to train the model for skin disease prediction.
- **Model Evaluation:** Uses accuracy, precision, recall, F1-score, and loss to evaluate performance.

## Model Architecture

The model consists of four main components:

1. **Image Encoder:** ResNet50 extracts features from skin disease images.
2. **Text Encoder:** BERT processes corresponding medical descriptions.
3. **Shared Embedding Space:** Projection layers map image and text features into a common vector space.
4. **Training and Classification:** Contrastive loss aligns corresponding image-text pairs, while classification loss trains the model to distinguish between skin conditions.

## Dataset

The project uses a labeled skin disease image dataset from Kaggle, paired with corresponding clinical descriptions.

The model focuses on six skin conditions:

- Eczema
- Melanoma
- Atopic dermatitis
- Basal cell carcinoma
- Seborrheic keratosis
- Warts and molluscum

The data is split into training, validation, and testing sets, with appropriate preprocessing applied to images and text.

## Results

The model achieved the following results on the test set:

| Metric | Score |
|---|---:|
| Test Accuracy | 97.01% |
| Weighted F1-Score | 0.9703 |
| Precision | 0.9727 |
| Recall | 0.9701 |
| Test Loss | 3.1959 |

These results demonstrate promising classification performance on the evaluated dataset. Further testing on diverse, independently collected clinical data is necessary to assess generalization to real-world settings.

## Technologies Used

- **Python**
- **PyTorch / Deep Learning Frameworks**
- **ResNet50**
- **BERT**
- **Contrastive Learning**
- **Natural Language Processing (NLP)**
- **Computer Vision**
- **NumPy and Data Visualization Tools**

*Update this list to match the exact libraries and frameworks used in your implementation.*

## Project Workflow

1. Collect and preprocess labeled skin disease images and clinical descriptions.
2. Split the dataset into training, validation, and test sets.
3. Extract image and text features using ResNet50 and BERT.
4. Project both modalities into a shared embedding space.
5. Train the model using contrastive and classification losses.
6. Monitor validation performance and adjust training parameters.
7. Evaluate the final model using classification metrics.

## Future Improvements

- Evaluate performance on independent, clinically validated datasets.
- Improve generalization across different skin tones and image conditions.
- Analyze confusion matrices to identify commonly misclassified conditions.
- Explore image-text similarity for retrieving relevant clinical descriptions.
- Investigate model calibration and uncertainty estimation.

## Limitations and Disclaimer

This project is an educational research project and is **not intended to provide medical diagnoses or replace professional medical advice**. Performance on a particular dataset does not guarantee clinical accuracy. Dataset quality, class imbalance, and differences between training images and real-world clinical images may affect results.

## Author

Developed as a student research project exploring multimodal machine learning, contrastive learning, and AI applications in dermatology.
