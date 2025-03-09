# CIFAR-10 Image Classification using CNN

#### side note:
I actually didn't read the General Instructions part of the pdf and just realized that I had to document everything while making tiny commits.
I have a half made CHIP 8 emulator already made in python lol if yall want to see https://github.com/thinkter/CHIP8/
## Overview
This project is an image classifier model built using Convolutional Neural Networks (CNN) to classify images from the CIFAR-10 dataset. The dataset consists of 60,000 images categorized into 10 classes:

**['airplane', 'automobile', 'bird', 'cat', 'deer', 'dog', 'frog', 'horse', 'ship', 'truck']**.

The model achieves an accuracy of approximately **78%** using a custom CNN architecture and explores an alternative approach using **Transfer Learning with VGG16**.

---

## Project Background
I'm relatively new to AI/ML, with my prior experience limited to training a YOLO model for object detection a while back. This project was an opportunity to get hands-on experience with CNNs and image classification.

I initially planned to implement hyperparameter tuning with `keras_tuner`, but due to setup issues and the simplicity of the model, I opted for manual tuning instead.

---

## Model Architecture
The model follows a simple CNN-based approach:
- Two **Convolutional + Pooling** blocks to extract distinguishing features.
- A **Flatten** layer to convert the feature maps into a 1D array.
- A **fully connected ANN** for classification.

### Data Preprocessing
- Loaded the CIFAR-10 dataset (50,000 training and 10,000 testing images).
- Normalized the RGB values for better convergence.

### Training Details
- **Initial Hyperparameters:**
  - Batch size: **64**
  - Learning rate: **0.001**
  - Accuracy achieved: **~78%**

- **Early Stopping:** Implemented but didn't make a significant difference in this case.

- **Manual Hyperparameter Tuning:**
  - Learning rate reduced to **0.0001**
  - Batch size increased to **128**

---

## Transfer Learning Attempt (VGG16)
I also attempted **Transfer Learning** using the VGG16 model. However, my implementation resulted in only **62% accuracy**, likely due to incorrect selection of additional layers on top of VGG16. This remains an area for further exploration.

---

## Performance Metrics
To evaluate the model, I computed:
- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**

Additionally, I visualized the **training and validation accuracy/loss curves** to analyze performance over epochs.

---

## Future Improvements
- Properly implement **hyperparameter tuning** with `keras_tuner`.
- Improve **Transfer Learning** by correctly fine-tuning additional layers on top of VGG16.
- Experiment with **data augmentation** to improve generalization.
- Try **deeper architectures** for better feature extraction.

---


## Final Thoughts
- learnt some new stuff
