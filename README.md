# limb-detection-framework
The minor project "Limb Movement Detection Framework"  is a deep learning based project that works upon the idea of  monitoring system for human activity recognition in various domains like public places, automated teller machines or healthcare sector. At recent times, deep learning has arisen as a group of deep architecture based learning models that render high level abstraction data. In this project we develop a framework using a Convolution Neural Network for detection and recognition of human activity types inside the premises. Typically, we would develop a framework through a layered structure that would be able predict the above mentioned activities (human activities)

Project 1:
First I experimented with th 5 activities dataset. I trained the upper layers of famous object detection models such as VGG-16, ResNet, GoogleNet, Densenet etc. trained on ImageNet dataset using transfer learning.

Project 2:
Next I trained a 2D-CNN model from scratch on 5 activities dataset. The model is there in the repo (my_model-limbdetections.pt). The code used for learning is final_minor_project.ipynb. I used the model for predicting activities from live video (the code for same is final_minor_project.ipynb) and used it to control many mouse and keyboard events using PyAutoGui library. I specifically embedded the activitiess in dino game in chrome.

Project 3:
I also experimented with Siamesem Neural Network idea for predicting activities using one-shot learning. The original Siamese Network is minor_project_human_activities.ipynb First I trained my siamese net on 15 activities dataset. The code for same is minor_project_human_activities.ipynb Then I modified the model slightly (basically made the model light so that it does not take much space) and after some hyperparameter tuning, I trained the model on 25 activities dataset. he link to model is siamese-model.txt. I got a whopping 98% 25-way validation accuracy. 

Project 4:
I also made a simple cat-vs-dog classifier that classifies the images as cat or dog and deployed it on web server using Flask and REST Api. The pretrained model is cats_vs_dogs_acc.h5. The main app is api2.py and the template is index3.html.

Details for implementation:
Project 1:
It was basically to get an idea of transfer learning and hyperparameter tuning using Tensorflow library. It can be implemented by downloading the 5-activities dataset and running the notebook (Change the path to dataset in the notebook and set it to where you have downloaded the dataset). You can also add more images in the set as per your convenience.

Warning: Do not try this without gpu. You can use google colab though as it provides free gpu.

Project 2:
It was to use the model for live video streams. If you want to train the model, download the activities-5 dataset and run the notebook minor_project_human_activities.ipynb (change the path to dataset) the trained model will be saved in your working directory.  

Project 3:
It was to implement the idea of one-shot learning to predict activities. To experiment with the 15-activities model, Download the 15-activities dataset and run the notebook (change the data-path in the notebook). Trained model is saved in the working directory. To train the model for 25-way prediction, download the 25 activities dataset and run the notebook minor_project_human_activities.ipynb(change the data-path). The trained model is saved in your working directory. 

Note: The directory structure should be

oneshot-test
train (one image per activity with name activity.jpg)
test (one test image)
Also it would be better if you add some more images in the 25-activities dataset to introduce more variance and retrain the model (only if you have a gpu instance).

Warning: The number of images in each gesture should be same and change shape of X in Siamese_handgestures_25_2.ipynb accordingly.

Project 4:
It was to get an idea of Flask and REST api. Download the cats_vs_dogs_acc.h5 and make the directory structure as follows-

Flask
api2.py
cats_vs_dogs_acc.h5
templates
index3.html
Open the terminal in required directory and run $python api2.py
