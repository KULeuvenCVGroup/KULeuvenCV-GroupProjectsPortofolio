# Face Recognition with Handcrafted and Learned Features

This project was developed as part of the Computer Vision course (H02A5a) at KU Leuven. It explores advanced techniques for constructing feature representations and performing face recognition using both handcrafted and data-driven methods. The work culminated in a Kaggle competition where we applied and evaluated our full pipeline.

## 📁 Project Overview

We developed a comprehensive face recognition pipeline that includes:

- **Preprocessing**: Face detection and alignment using OpenCV.
- **Feature Extraction**:
  - **Handcrafted**: Histogram of Oriented Gradients (HOG).
  - **Learned**: Principal Component Analysis (PCA) for eigenfaces.
- **Classification**: Multi-class and binary classifiers to distinguish between Jesse Eisenberg, Mila Kunis, and others.
- **Evaluation**: Accuracy on test data and qualitative analysis using t-SNE and PCA visualizations.
- **Kaggle Submission**: Final pipeline submitted to a course-specific Kaggle competition.

## 🧠 Assignment Objectives

This project addresses the following key questions:

- **Feature Construction**: How can we build effective feature representations using both handcrafted descriptors and features learned from data?
- **Classification Strategy**: How can these feature representations be utilized and compared within the context of classifying faces, particularly distinguishing between similar-looking individuals?
- **Pipeline Improvement**: What improvements can be made in face detection, feature extraction, and model classification to enhance overall performance?
- **Preprocessing and Data Quality**: What preprocessing steps are necessary to ensure clean, robust, and discriminative features?
- **Real-world Application**: How do these approaches translate to real-life scenarios where more training data may be available, but detection conditions are more challenging?

## 💡 Key Insights

- HOG features provided strong local structure representation but were sensitive to lighting and pose.
- PCA-based eigenfaces captured global facial characteristics and allowed dimensionality reduction.
- Combining robust preprocessing with discriminative features significantly improved classification accuracy.
- The Kaggle test set contained mislabeled or incorrect images, making perfect accuracy unattainable.

## 🛠️ Technologies Used

- Python
- OpenCV
- Scikit-learn
- Matplotlib / Seaborn
- t-SNE (via scikit-learn)
- Kaggle API

## 👥 Team Contributions

| Name              | Contribution                                                                 | Private Repo Link |
|-------------------|------------------------------------------------------------------------------|-------------------|
| John Ferderigos     | Implemented HOG feature extraction and visualization                         | GitHub |
| Vasileios Panagakis       | Developed PCA pipeline and eigenface visualizations                          | GitHub |
| Jordi Beltran Perello     | Built and evaluated classifiers, handled cross-validation                    | [GitHub](https://github.com/carolexample/cv-classe, managed Kaggle submissions, and documented experiments  | GitHub |
| Fotios Kalioras      | Preprocessing, face detection improvements, and final report writing         | GitHub |

> _Replace the names and links above with your actual team members and their GitHub repos._

## 📉 Limitations & Future Work

- The test set contained mislabeled images, limiting achievable accuracy.
- With more time, we would:
  - Explore deep learning models and embeddings.
  - Further refine preprocessing steps for robustness.
  - Investigate ensemble methods or hybrid feature strategies.
