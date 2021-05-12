# Image Classification for Dog Breeds
<img src="https://media1.s-nbcnews.com/i/newscms/2020_28/1587661/dogs-age-years-kb-inline-200707_7d0bca498155db9ae60dd81dec0ba6ab.jpg" alt= "dogs" >
Author: Anisha Malhotra

# Overview
This project applies Neural Networks to a dataset of dog images. In this project, each dog image is classified by its breed by training several models in efforts to determine the model with the highest accuracy score. 

# Business Problem
There are about 200 dog breeds in the world right now, which can make differing breeds from one another rather difficult. When dogs are rescued and taken to shelters, it can be benefical to determine which breed they are for medical reasons (certain breeds have different medical conditions) and so that they can find a forever home as fast as possible (if someone has a breed preference). Additionally, this classification system can also be useful to landlords who are renting out homes and only allow certain dog breeds due to liability.

# Data 
The data in this project was pulled from Kaggle and includes 20,580 images of 120 different dog breeds. The link to the data: https://www.kaggle.com/jessicali9530/stanford-dogs-dataset

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/imagesbreed.png?raw=true" alt= "imagecount" >
          
This plot shows the amount of images per breed. There is no significant class imbalance issue, however it is evident that the breed with the most images are Maltese and least is Redbone.

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/eda.png?raw=true" alt= "eda" >

Here are nine random images from the dataset to give examples of what the data contains.

There are many breeds that can be commonly confused. For example, Malamute and Siberian Huskies can look very similar. 

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/malamute-vs-husky.jpg?raw=true" alt= "sibhusky" >

Later, instances of predicting on these commonly mistaken dogs will be shown to see how the model performs.

# Process
 
After reading in the data as numerical arrays, the data was resized and scaled using various Tensorflow tools. The data was then augmented using Tensorflow's ImageDataGenerator and various version of each image were fed to the model (ex: zoomed in and flipped versions) to prevent the model from overfitting. 

# Model Evaluation

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/eval.png?raw=true" alt= "eval" >

After running several models, the model with the highest accuracy score is the InceptionV3 Model with an accuracy score of 96.12%. Plotted below are the accuracy and loss per epoch graphs for this model.

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/accuracy.png?raw=true" alt= "acc" >
<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/loss.png?raw=true" alt= "loss" >

# Predictions

Unseen images were passed to this model to test the accuracy of its predictions.

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/husky-wrong.png?raw=true" alt= "husky-wrong" >

Here is an image of a Malamute that the model wrongly predicted as a Siberian Husky, however the following is an image of a Siberian Husky that the model predicted correctly.

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/husky-right.png?raw=true" alt= "husky-right" >

Here are some other images the model predicted correctly.

<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/lab.png?raw=true" alt= "lab" >
<img src="https://github.com/anisha732/Phase5Proj/blob/main/photos/shihtzu.png?raw=true" alt= "shihtzu" >

# Next Steps
- Include images of mixed breeds within classes instead of just pure dog breeds (ex: cockapoo, puggle)
- Create a recommendation system that recommends similar breeds based on input image
- Create user interface that allows an input of an image

# Repository Structure
```
├── photos
├── DogClassificationPresentation 
├── Final_notebook.ipynb
├── Raw_Notebook.ipynb
└── README.md
```
