# In the Name of Deep Learning  
This project was developed as part of the Computer Vision course (H02A5a) at KU Leuven. It focuses on applying deep learning techniques to three core computer vision problems: **image classification, semantic segmentation, and adversarial attacks**. The work was evaluated through a Kaggle competition and extended analysis, where we compared methods and tested the robustness of our models.  

## Project Goal  
The main objective was to **develop, train, and analyze convolutional neural networks (CNNs)** for multiple vision tasks on the PASCAL VOC 2009 dataset, and to explore the vulnerabilities of these models to adversarial perturbations. This required building effective deep learning pipelines, optimizing them for performance, and critically evaluating their limitations.  

## Project Overview  
We implemented a three-part deep learning workflow:  
- **Image Classification**: Designed CNN architectures to classify images into 20 object classes. Compared training from scratch vs. transfer learning with pretrained networks.  
- **Semantic Segmentation**: Implemented encoder–decoder architectures (e.g., U-Net) to label every pixel in an image. Investigated the effect of skip connections and loss function choices.  
- **Adversarial Attacks**: Built a CNN adversary to perturb images in order to fool both classification and segmentation models, while keeping changes imperceptible to humans.  

## Assignment Objectives  
This project addresses the following key questions:  
- **Classification**: How can CNNs be structured and optimized to recognize diverse objects in complex scenes?  
- **Segmentation**: What architectures and design choices lead to accurate pixel-level labeling of images?  
- **Adversarial Robustness**: How can small, imperceptible perturbations drastically alter model predictions, and what does this reveal about the reliability of deep learning?  
- **Generalization**: Which strategies (augmentation, regularization, transfer learning) improve robustness across tasks?  
- **Real-world Impact**: How do these findings translate to real-world applications like autonomous driving or medical imaging?  

## Final Models & Methods  
### Image Classification  
- Implemented baseline CNNs from scratch.  
- Transfer learning with pretrained ResNet/EfficientNet for improved accuracy.  
- Data augmentation: flips, rotations, and color jitter to improve generalization.  
- Evaluation with accuracy, loss curves, and misclassification analysis.  

### Semantic Segmentation  
- Used U-Net–style encoder–decoder architecture.  
- Skip connections improved reconstruction of fine-grained details.  
- Cross-entropy and Dice loss compared for optimization.  
- Evaluation included Dice scores and qualitative analysis of segmentation masks.  

### Adversarial Attacks  
- Implemented a **CNN adversary** in an encoder–decoder setup to generate perturbations.  
- Perturbations were optimized under white-box conditions, with access to the gradients of the target models.  
- Loss terms balanced **(i)** fooling the classifier/segmenter and **(ii)** keeping perturbations small and imperceptible, using L₂/L∞ regularization norms.  
- Attacks successfully demonstrated how seemingly invisible noise could cause classifiers to mislabel objects and segmenters to produce misleading masks.  
- Visualizations included the clean image, perturbation, perturbed image, and model outputs.  

## Visualizations  
- **Training Curves**: Loss and accuracy progression across tasks.  
- **Confusion Matrices**: For classification, showing common class confusions.  
- **Segmentation Masks**: Predictions vs. ground truth, including failure cases.  
- **Adversarial Examples**: Before/after images with perturbations and resulting predictions.  

## 💡 Key Insights  
- Transfer learning dramatically boosted classification performance.  
- Skip connections and Dice loss were crucial for strong segmentation results.  
- The adversarial CNN highlighted major vulnerabilities, with models being easily fooled despite high validation accuracy.  
- Robustness remains a critical open challenge for deploying deep learning in safety-critical environments.  

## 🛠️ Technologies Used  
- Python  
- TensorFlow / Keras  
- Albumentations  
- Matplotlib / Seaborn  
- Scikit-learn  
- Kaggle API  

## 👥 Team Contributions  
| Name                | Contribution                                                                 | Private Repo Link |  
|---------------------|----------------------------------------------------------------------------|-------------------|  
| John Ferderigos     | Implemented CNNs for classification, tuned architectures and augmentation. | GitHub |  
| Jordi Beltran Perello | Developed and trained segmentation pipelines, including U-Net experiments. | [GitHub](https://github.com/jordibelp) |  
| Vassilis Panagakis | Designed and implemented adversarial attacks on classifiers and segmenters. | [GitHub](https://github.com/vm-panag) |  
| Fotis Kalioras     | Preprocessing, documentation, and integration of results into final notebook. | [GitHub](https://github.com/fothot2) |  

## Limitations & Future Work  
- Due to a heavy academic schedule, extensive experimentation with more architectures and training strategies was limited.  
- Future extensions could include:  
  - Exploring Vision Transformers (ViTs) for classification and segmentation.  
  - Systematic study of robustness under different adversarial scenarios.  
  - Ensembling multiple models for higher accuracy and stability.
