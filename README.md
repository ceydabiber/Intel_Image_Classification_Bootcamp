# Project Overview
This project is part of the Akbank Bootcamp: Introduction to Deep Learning. The goal is to classify images of different natural and artificial environments into six categories using deep learning models.

- **Dataset:** [Intel Image Classification](https://www.kaggle.com/datasets/puneet6060/intel-image-classification)  
- **Number of Classes:** 6 (Buildings, Forest, Glacier, Mountain, Sea, Street)  
- **Dataset Size:** ~25,000 training images, ~14,000 test images  
- **Task Type:** Multiclass Image Classification

## Models Used
1. **Custom CNN**  
   - Three convolutional layers followed by max-pooling  
   - Fully connected layers for classification  
2. **MobileNetV2**  
   - Pretrained transfer learning model with fine-tuning  

## Evaluation Metrics
| Model        | Accuracy | Precision | Recall | F1-score |
|--------------|---------|-----------|--------|----------|
| Custom CNN   | 0.8245  | 0.8273    | 0.8252 | 0.8256   |
| MobileNetV2  | 0.7797  | 0.7820    | 0.7821 | 0.7818   |

### Class-wise Performance (Custom CNN)
| Class      | Precision | Recall | F1-score | Support |
|------------|-----------|--------|----------|---------|
| Buildings  | 0.80      | 0.78   | 0.79     | 328     |
| Forest     | 0.93      | 0.95   | 0.94     | 340     |
| Glacier    | 0.75      | 0.81   | 0.78     | 360     |
| Mountain   | 0.75      | 0.78   | 0.77     | 376     |
| Sea        | 0.85      | 0.82   | 0.83     | 341     |
| Street     | 0.87      | 0.81   | 0.84     | 357     |

### Class-wise Performance (MobileNetV2)
| Class      | Precision | Recall | F1-score | Support |
|------------|-----------|--------|----------|---------|
| Buildings  | 0.82      | 0.80   | 0.81     | 328     |
| Forest     | 0.91      | 0.96   | 0.93     | 340     |
| Glacier    | 0.69      | 0.66   | 0.67     | 360     |
| Mountain   | 0.69      | 0.72   | 0.71     | 376     |
| Sea        | 0.72      | 0.77   | 0.74     | 341     |
| Street     | 0.85      | 0.78   | 0.81     | 357     |

## Observations
- The **Custom CNN** performed slightly better overall than MobileNetV2 in this project.  
- Both models struggled more with **Glacier** and **Mountain** classes, likely due to visual similarities and limited distinctive features.  
- Precision and recall were highest for **Forest** across both models.

## Improvements
- Adding **data augmentation** (rotation, zoom, flips) could improve model generalization.  
- Increasing training epochs and using **learning rate scheduling** might further boost accuracy.  
- Experimenting with more advanced architectures (ResNet, EfficientNet) could provide better feature extraction.

## Future Work 
- Explore **ensemble methods** combining multiple models to increase performance.  

## Links
- [Dataset on Kaggle](https://www.kaggle.com/datasets/puneet6060/intel-image-classification)
