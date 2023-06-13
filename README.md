# Explainable Diagnosis of Early Gastric Neoplasms under Endoscopy
This project develops an explainable AI method that not only offers prediction results for the diagnosis of early gastric neoplasm but also provides diagnostic evidence that aligns with the knowledge of endoscopists. It supports the diagnostic process by presenting interpretable information alongside the predictions. The framework for developing the method including feature extraction and multi-feature fitting, as shown below.
![image](https://github.com/Zuuuua/XAI-for-EGC-diagnosis/assets/135951585/14edd4cd-13c8-4f18-ab29-04b28b5cb59a)

# Tutorial
Before starting, please ensure you have the following:
Python 3.6+
Endoscopic images segmented by the minimum bounding rectangle encompassing the abnormalities. The lesions can be segmented using deep learning models such as YOLO or manually segmented.

## Step 1: Quantitative Analysis of Lesion Features
Navigate to the 'feature extraction_quantification' folder and run the provided .ipynb scripts. These scripts read the segmented images, perform quantitative analysis of lesion features (including shape, color, texture, etc.), and output feature labels. This steps is for extracting quantified features of lesions.

## Step 2: Deep Learning-Based Feature Extraction
Proceed to the 'feature extraction deep learning' folder. Run the 'data_preprocessing.ipynb' notebook to prepare the data required for the mean_teacher deep learning model. The output of 'data_preprocessing.ipynb' will serve as input for 'model_training_mean_teacher.ipynb'. This notebook trains the model using various parameters, and the model with the highest accuracy is selected and saved. You can test the models using 'model_testing.ipynb'. Additionally, use 'feature_combination.ipynb' to merge all the extracted features into a single sheet. This step is for extracting lesion features using deep learning methods.

## Step 3: Machine Learning Model Training and Testing
In the 'multi-feature-fitting' folder, input all the features extracted from the previous steps into the 'model_training.ipynb' notebook. This notebook trains machine learning models to diagnose gastric neoplasms. The best model with the highest accuracy will be saved and can be further evaluated using 'model_testing.ipynb'.

By following these steps, you will be able to utilize the explainable AI method for diagnosing early gastric neoplasms under endoscopy.

I acknowledge the help from Hao Li and Leanne Wu for building this method and coding.
