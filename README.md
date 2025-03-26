# DR_Cataract
Detecting eye diseases - Diabetic Retinopathy (DR) and Cataract by fine-tuning pretrained CNN models 

# Dual Detection of Diabetic Retinopathy and Cataracts Using Deep Learning

## Overview
Diabetic Retinopathy (DR) and cataracts are major causes of preventable blindness, yet most automated diagnostic systems focus on detecting only one condition at a time. This project introduces a **multi-task deep learning model** based on **VGG-16**, capable of simultaneously detecting **both DR and cataracts** from retinal fundus images. Our approach optimizes clinical efficiency by reducing computational overhead and screening costs, making it particularly useful for **low-resource healthcare settings** and **telemedicine platforms**.

## Features
✅ **Dual Disease Detection** – Simultaneous identification of **diabetic retinopathy** and **cataracts**.  
✅ **Pretrained CNNs** – Evaluated **EfficientNet, ResNet-50, and VGG-16** (VGG performed best).  
✅ **Optimized Image Preprocessing** – Applied **contrast-aware normalization, resizing, and noise reduction**.  
✅ **High Accuracy** – Achieved **93% accuracy**, with **F1-scores of 0.97 (DR) and 0.91 (Cataract)**.  
✅ **Computational Efficiency** – 40% lower overhead compared to sequential models.  

## Dataset
We utilized a publicly available dataset from **Kaggle**:  
🔗 [Dataset Link](https://www.kaggle.com/datasets/chowdhuryarman/armansc)  

- **Three classes**: Normal, Diabetic Retinopathy, Cataract  
- **Total images**: 3345  
- **Preprocessing**: Images resized to **224×224 pixels**, contrast-enhanced, and filtered to remove artifacts.  

## Model Comparison
We evaluated three **pretrained CNNs** on the dataset:  

| Model         | F1-Score |
|--------------|---------|
| **EfficientNet** | 0.87    |
| **ResNet-50**    | 0.89    |
| **VGG-16**       | 0.97    |

🔹 **VGG-16** outperformed other models in both **DR and cataract detection**, achieving the best overall accuracy.  

## Evaluation Results (VGG-16)
| Class                  | Precision | Recall | F1-Score | Support |
|------------------------|-----------|--------|----------|---------|
| Normal                 | 0.92      | 0.86   | 0.89     | 108     |
| Diabetic Retinopathy   | 0.97      | 1.00   | 0.98     | 124     |
| Cataract               | 0.90      | 0.92   | 0.91     | 103     |
| **Overall Accuracy**   | **0.93**  | 0.93   | 0.93     | 335     |

## Deployment
We plan to **deploy** this model as a **web application**, allowing easy access for clinicians and healthcare providers.

## Future Work
- **Federated Learning** for better generalization across diverse populations.  
- Integration with **telemedicine platforms** to facilitate remote diagnosis.  

## How to Use
1. Pick any of the ipynb file and save a copy on your google colab
2. You will need your own Kaggle account access token for the kagglehub api, as the notebooks directly download datasets from kaggle. 
3. Make sure you are using Google's free GPU. (it makes the code run faster)
4. For faster training, decrease the number of epochs. 
