## Exploratory Data Analysis (EDA)

The objective of this Exploratory Data Analysis (EDA) is to understand the structure,
distribution, and visual characteristics of the PlantVillage dataset before training
any machine learning model.

Through EDA, we aim to identify potential challenges such as class imbalance,
fine-grained visual differences between diseases, and dataset biases that could
impact model performance.

## Dataset Overview

The PlantVillage dataset consists of leaf images belonging to multiple plant species
and disease categories. Each class represents a specific disease or a healthy plant.

For this analysis, we use the original color images, as disease symptoms are often
characterized by color changes such as spots, discoloration, or lesions.

## Class Distribution

We analyze the number of images available for each disease class to understand
whether the dataset is balanced.

The class distribution shows noticeable imbalance, with some disease categories
having significantly more samples than others. This imbalance may cause a trained
model to favor majority classes while underperforming on minority classes.

**Insight:** Class imbalance suggests the need for data augmentation or class-weighted
loss functions during training.

## Visual Inspection of Sample Images

To gain a human-level understanding of the dataset, we visualize multiple images
from each disease class.

From the samples, we observe that several disease classes exhibit visually similar
symptoms, such as small spots or subtle color changes. Additionally, most images
have clean and uniform backgrounds, which may simplify the classification task
but could reduce generalization to real-world images.

**Insight:** The presence of visually similar disease patterns makes this a fine-grained
classification problem, requiring models capable of learning subtle visual features.

## Image Resolution and Size Analysis

We analyze image width and height to understand resolution consistency across
the dataset.

Most images have similar resolutions, with limited variation in aspect ratios.
This consistency allows for standard resizing during preprocessing without
significant distortion of visual features.

**Insight:** Consistent image sizes simplify preprocessing and support the use of
fixed-input CNN architectures.

## Dataset Bias and Quality Considerations

The majority of images are captured in controlled environments with minimal
background clutter and good lighting conditions.

While this improves visual clarity, it introduces a dataset bias, as real-world
field images may contain complex backgrounds, shadows, and occlusions.

**Insight:** Strong background consistency may lead the model to rely on background
features instead of disease patterns, highlighting the importance of robust data
augmentation.

## Summary of EDA Findings

Based on our exploratory analysis, we identify the following key challenges:

1. Class imbalance across disease categories
2. Fine-grained visual similarities between different diseases
3. Uniform backgrounds that may reduce real-world generalization

These observations will guide preprocessing choices, augmentation strategies,
and model architecture selection in subsequent stages of the project.

