# 🦠 Lung Cancer Detection Using CT Scans

## 📄 Project Overview

Lung cancer is one of the leading causes of cancer-related deaths worldwide, largely due to the difficulty of detecting it in its early stages. Early diagnosis through medical imaging, particularly Computed Tomography (CT) scans, can greatly improve patient outcomes. This project explores the application of deep learning models in automating the detection of lung cancer from CT images, comparing the effectiveness of several pre-trained models and a custom-built model.

## 🔍 Problem Statement

Lung cancer accounts for approximately 25% of all cancer deaths, making it one of the deadliest forms of cancer. The manual analysis of CT images is not only time-consuming but also prone to human error, which can lead to late-stage diagnosis when treatment options are limited. The aim of this project is to leverage deep learning models to automate the detection process, providing a tool that can assist in the early diagnosis of lung cancer.

## 💡 Importance of the Project

Early detection of lung cancer through automated CT scan analysis can save lives by allowing for earlier intervention. This project demonstrates how deep learning can be applied to medical imaging to enhance diagnostic accuracy, reduce the burden on healthcare professionals, and improve patient outcomes. Additionally, the project includes a user-friendly interface to make the models accessible to a wider audience, including healthcare providers who may not have technical expertise.

## 📊 Models and Approach

This project compares the performance of three pre-trained models—VGG16, VGG19, and AlexNet—with a custom Keras model built from scratch. The models were trained and evaluated using a dataset of lung CT images, with metrics such as accuracy, precision, recall, AUC, and F1 Score used to assess their performance. An ensemble model was also created using majority voting to combine the predictions of the three pre-trained models, further enhancing detection accuracy.

## 🛠️ Methodology

### Data Preprocessing
- **Histogram Equalization**: Applied to improve the contrast of CT images.
- **Segmentation**: Used to isolate lung tissues from the background.
- **Normalization**: Images were resized and normalized to prepare them for model input.

### Model Training
- **Pre-trained Models**: VGG16, VGG19, and AlexNet were adapted for lung cancer detection by adding custom layers on top of their pre-trained convolutional layers.
- **Custom Model**: A Keras model was built from scratch with multiple convolutional, pooling, and fully connected layers.
- **Ensemble Model**: Majority voting was used to combine the predictions of the three pre-trained models to enhance overall accuracy.

### User Interface
A Gradio interface was developed to allow users to upload CT images and receive predictions from all the models. The interface also displays the accuracy of each model, providing a practical demonstration of how these models can be applied in real-world scenarios.

## 📈 Comparative Analysis

The project includes a comprehensive analysis of the models, comparing their performance using key metrics like accuracy, precision, recall, AUC, and F1 Score. The analysis helps in understanding which model performs best and why, offering insights into the effectiveness of deep learning in medical imaging.

## 🗂️ Project Structure

## 🗂️ Project Folder Structure

data/ 

├── raw_data/

│   ├── adenocarcinoma/

│   ├── largeCellCarcinoma/

│   ├── normal/

│   └── squamousCellCarcinoma/

├── processed_data/

│   ├── train/

│   │   ├── non-cancerous/

│   │   └── cancerous/

│   ├── val/

│   │   ├── non-cancerous/

│   │   └── cancerous/

│   └── test/

│       ├── non-cancerous/

│       └── cancerous/

└── Colab Notebooks/

    └── lung-detect-CT.ipynb



## 💻 How to Use This Project

### Prerequisites
- A Google Drive account is required to store and access the dataset.
- Set up your Google Drive with the folder structure provided above.

### Instructions
1. **Clone the Repository**: Download the project files from this GitHub repository.
2. **Data Preparation**: Upload your CT image dataset to your Google Drive following the provided folder structure.
3. **Preprocessing**: Run the preprocessing steps to prepare your images for model training.
4. **Training and Evaluation**: Use the provided Jupyter notebook (`lung-detect-CT.ipynb`) to train and evaluate the models.
5. **Model Predictions**: Use the Gradio interface to interact with the trained models and see predictions on new CT images.
6. **Comparative Analysis**: Review the comparative analysis to understand the performance of different models.

## 🙌 Acknowledgements

This project builds on the work of many researchers who have explored the application of deep learning in medical imaging. We extend our gratitude to the contributors of the datasets and the developers of the pre-trained models used in this study.

## 📜 License

This project is licensed under the MIT License.
