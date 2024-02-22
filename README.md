# phase4_project
# Pneumonia Identification using Image Classification: Phase4_Project

![image](https://github.com/ldwilker10/phase4_project/blob/main/images/dr_lungs_image.jpeg)


#### Project by: Lucas Wilkerson
#### Date: 2/21/2024 

## Project Overview
For this project, the aim is to build a model for image classification that can classify whether a patient has pneumonia when provided a chest x-ray image. 

## Business Problem/Stakeholder
A healthcare physician group is looking to improve their patient outcomes, specifically patients who are being diagnosed with pneumonia. Pneumonia is a significant health concern among patients, especially geriatric and pediatric patients. For effective treatment and the best possible outcomes, early detection and diagnosis is crucial. Current methods for diagnosing pneumonia can be time-consuming and can be prone to error. Through the development and use of method such as image classification and deep learning, we may be able to improve this process which can lead to an increase in early accurate identification and as a result improve patient outcomes.

## Data Understanding 

For this project, the aim is to build a convolution neural network (CNN)  model for image classification that can classify whether a patient has pneumonia when provided a chest x-ray image. A Kaggle dataset containing 5856 chest x-ray images was utilized to construct this model. The chest X-ray images were from pediatric patients with or without pneumonia who are ages one to five and were split into 3 separate datasets: 

- Train (5216 images): data used for training the model
- Test (624 images): data used for testing and evaluating the model's performance 
- Validation (16 images): data used during the training process to help tune the model

![image](https://github.com/ldwilker10/phase4_project/blob/main/images/train_set_distribution.png)

## Data Preparation 

Before building the model, the data underwent several preprocessing steps including:
- Data distribution analysis to understand the class balance or imbalance
- Visualizing sample images to get a visual sense of the data
- Checking the image dimensions to ensure they were suitable for the model.

During data preparation and preprocessing: 
- ImageDataGenerator from Keras was used for data augmentation to increase class diversity
- All images were rescaled and normalized to the range [0,1]
- Class imbalance was accounted for by balancing class weights

The data was also subsampled for the modeling process to allow for shorter computation run times. Twenty percent of the data was used for training. 



## Modeling 

Baseline Model: The initial baseline model was a simple convalutional neural network model. The basic architecture comprises convolutional layers with increasing filters, followed by max-pooling layers to capture features. Flattened outputs are fed through dense layers. The model is compiled with binary cross-entropy loss and trained for ten epochs using training and validation data, enabling it to learn and enhance its classification capabilities over time. The main metrics used to evaluate model performance included accuracy and recall. Overall the baseline model performance was not the best. 

The baseline model was iterated over multiple times by adjusted different parameters and applying different techniques such as regularization, adjusting learning rate and adding complexity by increasing filters. 


## Evaluation
### Best Model Results 

Looking at the best model, it had the same initial architecture as the baseline model with adjustments made to the learning rate and to number of filters in the convalutional layers. Learning rate was adjust to 0.001 and filter numbers were doubled compared to the baseline model. 


| Metric                  | Baseline                          | Best Model                        |
|-------------------------|-----------------------------------|-----------------------------------|
| Train Accuracy          | 0.8111                            | 0.8773                            |
| Test Accuracy           | 0.7500                            | 0.8221                            |
| Train Loss              | 0.4179                            | 0.2917                            |
| Test Loss               | 0.6010                            | 0.5218                            |
| Train Recall            | 0.7510                            | 0.8348                            |
| Test Recall             | 0.6513                            | 0.8103                            |


### Regarding the Best Model Scores:

Metrics of focus
- Recall score: 0.8103
- Accuracy: 0.8221

Accuracy: The model's overall accuracy score was 0.8221 which indicates that the model correctly labeled ~82% of the chest x-ray images that were observed in the test group.

Recall: The model's overall recall score was 0.8103 which means that out of all of the individuals/patients that actually had pneumonia, the model correctly identified ~81% of those.
 
Example of image with Pneumonia

![image](https://github.com/ldwilker10/phase4_project/blob/main/images/pne_image.png)

Example of image without Pneumonia

![image](https://github.com/ldwilker10/phase4_project/blob/main/images/no_pne_image.png)


## Conclusion/ Recommendations 


Recommendations: 

- Healthcare providers should utilize this model as a tool for early pneumonia detection. While this model is not an official diagnostic tool for penuamonia, this model is useful for early detecton and screening and can be cross-reference with professional physician observations.  

- Using this model, practitioner's can implement preventative health strategies to their patient population early on before disease progression and improve overall health outcomes. 


## Limitations

- False positives: With recall, there is the chance for more false positive results (individuals being classified as having pneumonia who in fact do not). While this can be a limitation at times, this is not a huge hinderance in this context because we would rather correctly identify positive cases than to not identify someone with pneumonia and they get left untreated. 

- Run time/ Model complexity: As model complexity increases, this does increase the requirement for computation power and can increase model run times. 

- Small sample size: With more data and more images to analyze, a more robust model could be utilized to increased accuracy.

## Contact Information

- Email: ldwilker10@gmail.com

- GitHub: https://github.com/ldwilker10

- LinkedIn: https://www.linkedin.com/in/lucasdukewilkerson/ 

## Repository Structure

├── chest_xray
├── draft_models    
├── images   
├── .gitignore                                                                                                                   
├── [README.md](https://github.com/ldwilker10/phase4_project/blob/main/README.md)                                          
├── [pneumonia_image_classification.pdf](link)       
└── [phase4_final_notebook.ipynb](link)  