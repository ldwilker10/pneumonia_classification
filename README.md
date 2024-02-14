# phase4_project
# Pneumonia Identification using Image Classification: Phase4_Project

![image](link)


#### Project by: Lucas Wilkerson
#### Date: 

## Project Overview
For this project, the aim is to build a model for image classification that can classify whether a patient has pneumonia when provided a chest x-ray image. 

## Business Problem/Stakeholder
A healthcare physician group is looking to improve their patient outcomes, specifically patients who are being diagnosed with pneumonia. Pneumonia is a significant health concern among patients, especially geriatric and pediatric patients. For effective treatment and the best possible outcomes, early detection and diagnosis is crucial. Current methods for diagnosing pneumonia can be time-consuming and can be prone to error. Through the development and use of method such as image classification and deep learning, we may be able to improve this process which can lead to an increase in early accurate identification and as a result improve patient outcomes.


## Data Understanding 

The dataset used for this project contains chest X-ray images from pediatric patients with or without pneumonia who are ages one to five. The dataset is already separated and organized into three groups, the train, test and validation groups. Looking at the whole dataset, there is a total of 5856 images. The training set contains 5216 images, the validation set contains 16 images and the test set contains 624 images. 

- Train: The training set has 3875 images labeled with pneumonia while having 1341 labeled as normal/without pneumonia. This image set seems to have an imbalanced class distribution since there are a long more images with pneumonia. This class imbalance could affect the model's performance and ability to generalize over the data so this will be addressed in the modeling process through data augmentation adn balancing the class weights. 
  
- Test: The test set has 390 images labeled with pneumonia while having 234 labeled as normal/without pneumonia. This image appears to have a more balanced distribution in comparison to the training set. Even though the the pneumonia images count is still higher than the images without pneumonia, the difference is not as vast as the training set.
  
- Validation: The validation set has small number of images for both classes with 8 images labeled with pneumonia while having 8 labeled as normal/without pneumonia.




![image](link)


## Modeling 

Baseline Model: The initial baseline model was a simple neural network model with ____


Convolutional Neural Network Model:


## Evaluation
### Best Model Results 

Looking at the modeling and models built, overall the baseline model seemed to perform the best when accounting for all metrics. With the baseline CNN model test accuracy was highest at ~84% with a test recall at ~ 84%. Train accuracy was at ~90% and train recall at ~87%. While these are slightly higher than the test metrics showing slight overfitting, this was more ideal than other models which were showing signs of higher degrees of overfitting and lower performance on test sets.

- Test Loss: 0.4282
- Test Accuracy: 0.8365
- Test Recall: 0.8359
- Train Loss: 0.2443
- Train Accuracy: 0.8984
- Train Recall: 0.8684



| Metric                  | Baseline                          | CNN Model                         |
|-------------------------|-----------------------------------|-----------------------------------|
| Train Accuracy          | 0.8984                            | 0.                                |
| Test Accuracy           | 0.8365                            | 0.                                |
| Train Loss              | 0.2443                            | 0.                                |
| Test Loss               | 0.4282                            | 0.                                |
| Train Recall            | 0.8684                            | 0.                                |
| Test Recall             | 0.8359                            | 0.                                |


### Regarding the Best Model Scores:
Metrics of focus
- Recall score, accuracy 

Accuracy: The model's overall accuracy score was 0.8365 which indicates that out of all the times that the model correctly labeled ~84% of the chest x-ray images that were observed in the test group.

Recall: The model's overall recall score was 0.8359 which means that out of all of the individuals/patients that actually had pneumonia, the model correctly identified ~84% of those. 
 

![image](link)


![image](link)


## Conclusion/ Recommendations 


Recommendations: 

- Healthcare providers should utilize this model as a tool for early pneumonia detection. While this model is not an official diagnostic tool for penuamonia, this model is useful for early detecton and screening. 

- Using this model, practitioner's can implement preventative health strategies to their patient population early on before disease progression and improve overall health outcomes. 

- In the context of identifying pneumonia. 


## Limitations
- Small sample size: With more data and more images to analyze, a more robust model could be utilized to increased accuracy.

- Run time/ Model complexity: As model complexity increases, this does increase the requirement for computation power and can increase model run times. 


## Contact Information

- Email: ldwilker10@gmail.com

- GitHub: https://github.com/ldwilker10

- LinkedIn: https://www.linkedin.com/in/lucasdukewilkerson/ 

## Repository Structure

├── chest_xray    
├── images   
├── .gitignore                                                                                                                   
├── [README.md](https://github.com/ldwilker10/phase4_project/blob/main/README.md)                                          
├── [pneumonia_image_classification.pdf](link)       
└── [phase4_final_notebook.ipynb](link)  