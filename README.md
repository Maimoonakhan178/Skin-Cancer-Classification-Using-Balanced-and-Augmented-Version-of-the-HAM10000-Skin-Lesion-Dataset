# Skin-Cancer-Classification-Using-Balanced-and-Augmented-Version-of-the-HAM10000-Skin-Lesion-Dataset

I worked on a project focused on classifying skin cancer using the HAM10000 dataset. This dataset contains 7 classes of skin lesions with highly imbalanced distributions. To address this, I designed and implemented a preprocessing strategy to ensure balanced class representation reducing overfitting and bias for fair model performance.

Dataset
The dataset was obtained from Mendeley Data: https://data.mendeley.com/datasets/hpcf9psdy7/1

It includes over 10,000 dermoscopic images categorized into 7 diagnostic classes.
However, it suffers from strong class imbalance:

Some classes contain 2,000–3,000+ images

Others have only 100–200 samples

Balancing Strategy
To address this imbalance, I applied a controlled balancing approach:

Threshold: 500 images per class

Downsampling: For classes with >500 samples

Augmentation: For smaller classes using realistic transformations — rotation, flipping, scaling, brightness adjustment, etc.

This combination created a balanced dataset while maintaining natural image diversity, avoiding unrealistic overfitting.

Hybrid Model Architecture
I implemented a ResNet–Transformer Hybrid Model to leverage both local and global feature extraction:

ResNet: Efficient in local texture and pattern recognition (key for medical images)

Transformer: Captures long-range dependencies and contextual relationships

This hybrid approach improved both accuracy and feature representation, proving effective for complex medical image classification tasks.

Results

Hybrid Model (ResNet + Transformer): 98% Accuracy

FixCap Benchmark Model: 96% Accuracy

Key Insights

The balanced dataset (via combined downsampling + augmentation) significantly reduced bias and improved generalization.

The hybrid model achieved superior accuracy through complementary feature learning.

Such collaborative deep learning architectures hold strong potential for medical AI applications requiring precision and interpretability.
