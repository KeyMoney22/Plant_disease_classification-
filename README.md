# Plant_disease_classification
![image](https://github.com/user-attachments/assets/ae644a5b-6bad-4b08-a941-861cb9681bc6)
## Introduction
Tomatoes are one of the most important crops in Kenya, both economically and nutritionally. They are a staple in the diet of many Kenyans and a significant source of income for smallholder farmers. However, tomato production in Kenya faces numerous challenges, among which diseases are the most important. Tomato plants are susceptible to various diseases caused by fungi, bacteria, viruses, and pests. These diseases can lead to substantial yield losses, reduced produce quality, and increased production costs due to the need for pesticides and other control measures.

The consequences of unchecked tomato diseases are severe. Yield losses can range from 20% to 100%, depending on the type and severity of the disease. This not only affects the income of farmers but also threatens food security and nutrition for millions of Kenyans. Addressing tomato diseases effectively is therefore crucial for enhancing agricultural productivity, improving the livelihoods of smallholder farmers, and ensuring food security in Kenya.

## Business Understanding

Agriculture is a cornerstone of Kenya's economy, with a majority of the population relying on it for their livelihood. However, plant diseases pose a significant threat to crop yields, leading to economic hardships for farmers and contributing to food insecurity. Traditional methods of disease detection are often slow, costly, and require expert knowledge.Developing an automated plant disease detection system using image recognition technology is crucial. This solution will enable Kenyan farmers to quickly and accurately identify diseases, take timely actions, and improve crop productivity, ultimately enhancing food security and supporting the country's agricultural economy.

### Objective

Develop an automated plant disease detection system leveraging image recognition technology. This solution aims to provide an accessible, cost-effective, and rapid method for farmers to diagnose plant diseases by analyzing images of crop leaves. By offering timely and accurate disease identification, this system can empower farmers to implement effective treatment strategies, minimize crop losses, and enhance agricultural productivity.


## Data Understanding

### Data Source

Our dataset was downloaded from a Kaggle repository authored by Plant Village.

PlantVillage is an organization hosted by Penn State University, is a research initiative focused on enhancing agricultural resilience and sustainability, particularly in the context of climate change. The platform employs advanced technologies such as artificial intelligence and data analytics to address various agricultural challenges including plant disease, which will be the focus of this project.
For this project we shall focus on Tomato Leaves.

The link to the repository is here: https://www.kaggle.com/datasets/emmarex/plantdisease?select=PlantVillage

Dataset Author Website: https://plantvillage.psu.edu/


### Other Objectives
i. Data Collection and Preprocessing.Gather and preprocess a diverse dataset of tomato leaf images.

ii. Model Development.Build and train deep learning models for disease classification.

iii. Model Evaluation.Assess the models performance using metrics such as accuracy

iv. Deployment



### Metrics of success
1. Model Accuracy: Achieve a classification accuracy of over 90%.


## Methodology
The project will follow the following steps:

a. **Exploratory Data Analysis:** We preview data and check the specifc class distributions and  clean the data 

b. **Data Preprocessing:** This step involves handling class imbalance , and resizing images 

c. **Model Selection and Training:** Trin various Tensorflow models, such as CNN, Resnet50, VGG19, Effiecientnet and MobilenetV2 to select the most suitable model tomato disease detection.

d. **Model Evaluation:** We will assess the performance of the trained models using  the accuracy metric and plot the tanining and validation performance of various models.

e. **Model Tuning:** We will fine-tune the top 2 models by adjusting hyperparameters and employing techniques wandb

f. **Model Deployment**

## EDA
![image](https://github.com/user-attachments/assets/dce0178c-4477-4b9e-af38-f1ca3ad036de)

**Observations**

The image displays nine image samples with corresponding class labels. The labels are  cleaned and formatted correctly based

![image](https://github.com/user-attachments/assets/d2989640-7b3b-46a5-a3a4-1b9e7757a942)

**Observations**

The horizontal bar chart shows the distribution of images across different classes in the dataset. Each bar represents a class, and its length corresponds to the frequency or count of images belonging to that class.tomato_yellow_leaf_curl_virus is the largest class containing 3208 images and tomato_mosaic_virus is the smallest class containing 373 images

## Modelling
### CNN Base Model 

![image](https://github.com/user-attachments/assets/ea2432c2-cf2a-4249-868a-95b836ab755e)

![image](https://github.com/user-attachments/assets/89eb0bab-1558-4ba7-8f39-b11f0c1435bb)

The model shows consistent improvement in both accuracy and loss on the training data, indicating effective learning.

The validation accuracy and loss trends suggest good generalization, and the fluctuations indicate variability in the validation data.

The difference between training and validation performance is relatively small, suggesting that the model generalizes well to unseen data, but there might be room for improvement to reduce overfitting.

**CNN Model Evaluation on Test (Unseen) Data**

Achieved a test accuracy of 91.4% indicates that the model, after several epochs of training and validation, performs  well on new, unseen data. This result shows that the model not only improved its performance on training and validation sets but also generalized well to the test set.

### VGG19 Model

![image](https://github.com/user-attachments/assets/8f8e9cce-3044-43eb-846f-4c0619cbeaa2)

![image](https://github.com/user-attachments/assets/18099fb4-948a-4a6b-9437-39d44706bc02)

The model is learning well on the training data, as seen by the increasing training accuracy and decreasing training loss.

The validation accuracy and loss suggest that the model generally performs well on unseen data but has some fluctuations indicating periods of slight overfitting.

**CNN Model Evaluation on Test (Unseen) Data**

The VGG19 model achieved a test accuracy of approximately 88.5%.It performs well and has strong generalization abilities.
