# TOMATO DISEASE DETECTION
![image](https://github.com/user-attachments/assets/ae644a5b-6bad-4b08-a941-861cb9681bc6)

**Authors:** Diana Olulo, Lisa Mwikali, Kimani Irungu, Purity Kibaki, Andrew Baraka, Victor Keya
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

The horizontal bar chart shows the distribution of images across different classes in the dataset. Each bar represents a class, and  count of images belonging to that class.tomato_yellow_leaf_curl_virus is the largest class containing 3208 images and tomato_mosaic_virus is the smallest class containing 373 images

## Modelling
**Quick preview of the base model and top 2 best perfoming models**

### CNN Base Model

![image](https://github.com/user-attachments/assets/249705be-0056-4b2e-bca4-4edce75a4fa5)

![image](https://github.com/user-attachments/assets/e34038cd-6e1b-45c7-8dc4-cd8b79bfc9d9)

- Both training and validation accuracy increase rapidly during the early epochs, suggesting that the model is learning effectively from the training data.
- Both training and validation loss decrease during the early epochs, indicating that the model is learning to make better predictions.
- The training accuracy consistently sits above the validation accuracy, indicating that the model is overfitting to the training data.

### ResNet50 Model

![image](https://github.com/user-attachments/assets/da087c23-040a-4e66-b377-ada3c862bd61)

![image](https://github.com/user-attachments/assets/00a324a8-a20f-424d-8ff1-f412f979949b)

- The training accuracy increases steadily from around 72.5% to around 88% over the 5 epochs indicating that the model is learning from the training data and improving its performance over time.
- The validation accuracy starts high, increases, and then slightly fluctuates but generally trends around 90%.This suggests that the model initially performs well on unseen data and maintains good performance, with minor fluctuations possibly due to data variability.
- The training loss decreases consistently from around 0.75 to around 0.25 over the epochs indicating that the model is learning to reduce errors on the training data.
- The validation loss starts lower than the training loss and fluctuates but shows a general downward trend suggesting that the model performs well on the validation set

### Resnet Hypertuned Model

![image](https://github.com/user-attachments/assets/33f67b04-9514-4e4e-ad27-2af88f20621f)

![image](https://github.com/user-attachments/assets/3971476b-bd9f-46c2-aba4-abbd420d5aa3)

- The training accuracy starts low at around 80% and increases steadily over the epochs, reaching approximately 94.8% by the end.
- The validation accuracy shows more fluctuations compared to the training accuracy.It starts high, dips slightly around the 3rd epoch, and then fluctuates but generally trends upwards.Despite these fluctuations, the validation accuracy also ends around 94.6%.
- The training loss starts relatively high around 0.6 and rapidly decreases over the epochs.
- The validation loss also starts high, around 0.4, and shows some fluctuations but generally trends downwards
  
## Model Evaluation

![image](https://github.com/user-attachments/assets/d910a9da-cfc7-4e37-a87e-b49d68b54653)



### Model Selection

ResNet50 is the best model due to its higher accuracy, consistent learning behavior, and better generalization capabilities compared to VGG19 and CNN model.

## CONCLUSION
-Resnet50 Model conistently showed the best performance with it getting to a training accuracy of 98% and a validation accuracy of 94.6% after hyperparametertuning was done.
- EfficientNet-B0 Model seemed to be performing well at certain points of the data and performing poorly at other points of the data with it achieving accuracies as low as 20% and very high losses indicating that it was not fitting well to the data.
- The VGG19 model's accuracy remained low , indicating challenges in model performance and optimization.
- CNN showed a moderate level of effectiveness but showed aspects of overfitting when tuning was done on it to try and improve its effectiveness.
- MobileNet V2 had the least impressive performance with it consistently performimg poorly against the data

## RECOMMENDATIONS
- Ensemble Methods:combining the predictions of multiple models to improve the overall accuracy and reduce the likelihood of overfitting
- Model Optimization:experiment with different learning rates, batch sizes, and epochs to enhance performance.
- Data Augmentation:incorporate more data augmentation techniques to increase the diversity of the training dataset, which can help improve the model's robustness and generalization.

## NEXT STEPS
- Enhancing the model to not only detect the presence of tomato diseases but also classify the severity of the infection (e.g., mild, moderate, severe). This information can help farmers prioritize treatment for more severely affected plants.
- Developing a mobile application that integrates the disease detection model. This app can allow farmers to take pictures of their tomato plants and receive instant feedback on disease presence, type, and severity, along with treatment recommendations.
- Integrating the model with Internet of Things (IoT) devices for continuous monitoring of tomato crops. Sensors and cameras can capture data and images in real-time, allowing the model to provide ongoing assessments and alerts for early disease detection.
- Creating training materials and resources to educate farmers on how to use the disease detection tools effectively. This can include tutorials on the mobile app, best practices for capturing images, and guidelines for interpreting the results.
