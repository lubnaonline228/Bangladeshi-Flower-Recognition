# A Bangladeshi Flower Recognizer
This repository contains files and documents for an application that uses Machine Learning to recognize Bangladeshi flowers. 

## Problem Statement
Bangladesh is home to a diverse a large variety of flowers. As such, a flower recognition application tailored to identify Bangladeshi flowers serves as a valuable tool for both enthusiasts and professionals. For hobbyists, it enhances the experience of nature walks and garden visits, offering instant knowledge about the flowers they encounter. Moreover, for researchers and environmentalists, the app accelerates species identification, facilitating biodiversity surveys and conservation initiatives. Given the rich cultural significance of flowers in Bangladeshi traditions, this app also fosters a deeper connection to the country's natural heritage, promoting appreciation and stewardship of its floral diversity.

The goal of this project is to create and train a model that can recognize 10 different types of Bangladeshi flowers:
1. Beli
2. Gada
3. Joba
4. Kamini
5. Kodom
6. Palash
7. Rose
8. Sheuli
9. Sunflower
10. Water Lily

## Data Scraping
Leveraging fastAI's DuckDuckGo search functionality, I implemented a loop to systematically collect images for each flower category, organizing them into respective folders. The entire data collection procedure is documented in the "data_collection" notebook for reference.

## Data Cleaning
Numerous duplicate images were found across multiple categories, and occasionally, images were misplaced between categories too. So, prior to training, it was necessary to eliminate these redundant images and ensure that each image was correctly placed within its designated folder. Following model training, when the outcomes fell short of expectations, I identified the classes with the highest losses and revisited the cleaning process. I also took the time to manually clean out the dataset to ensure better training. 

## Preparing the Data Loader
I divided the entire dataset into 80% for training and 20% for validation. Then, I set up the dataloader with a batch size of 32. Following the training process, I reviewed the categories with the most loss and refined the data multiple times to improve the results. Additionally, I generated multiple versions of the dataloader for further experimentation.

## Model Training
For constructing the classifier, I opted for several pre-trained computer vision models equipped with feature extractors accessible in fastAI's Vision Learner function, and proceeded to train them. The chosen models include:
* VGG-16
* ResNet-34

## Performance Evaluation

## Deployment
As ResNet-34 was showing better performance,I deployed the recognizer using the Gradio app within Huggingface. Check out the deployment & required files for the deployment.
