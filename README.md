# Muzic - Facial emotion detection based music recommendation system

### Table of Contents
1. [About the Project](#about)
2. [Features](#features)
3. [Dependencies](#dependencies)
4. [Instructions](#instructions)
4. [System Architecture](#system-architechture)
5. [Structure of this repository](#repository-structure)
6. [Future Scope](#future-scope)
7. [References](#references)


### About
This repository demonstrates an end-to-end pipeline for real-time Facial emotion recognition application along with reccommending music based on detected emotions.
Done in three steps:
1. Face Detection: from the video source using OpenCV.
2. Emotion Recognition: using a model trained by using Mediapipe library.
3. Music Recommendation: Using detected emotion to create a search query on Youtube

The model is trained for 50 epochs and runs at 87% accuracy.
![image](https://user-images.githubusercontent.com/81975567/170823927-bd313103-7b34-42fd-9635-1b913ec65667.png)


### Features
1. Landing Page
![image](https://user-images.githubusercontent.com/81975567/170835333-7a69618e-3f3c-46e9-90b1-b6fc72cc5553.png)

Seamless landing page filled with dark-theme.

2. Detection of various emotions like [Sad, Angry, Happy, Neutral, Surprise]


3. Detection of various gestures like [Hello, Thumbsup, Nope, Rock]





### Dependencies
This project depends on Python and following packages which can be easily installed through `requirements.txt` file by running the following command:
`pip install -r requirements.txt`
- Python 3.9.6
- pip 22.1.1
- streamlit 1.9.1
- streamlit-webrtc 0.37.0
- opencv-python 4.5.5.64
- mediapipe 0.8.10
 
### Instructions
#### Testing Locally
-	`git clone https://github.com/Sandeepimandi/Muzic`
-	Run `pip install -r requirements.txt` to install all dependencies.
-	`cd ./muzic`
-	`streamlit run Muzic_app.py`
-	The app is now running at http://localhost:8501
-	While testing, wait for the model to detect your emotions and click on recommend button to get songs based on a particular emotion
- Emotion used previously are stored as cache and might cause an error in recommending music, delete `detected_emotion.npy file` in the directory to resolve this. 
- Recommended music is loaded in next tab as a youtube search query.

### System Architechture
![image](https://user-images.githubusercontent.com/81975567/170823667-70ffb002-f1bd-4578-b9a0-4ed32baee51d.png)

### Repository Structure
 This repository is organised as:
 - [app](/app.py) This file contain the setup of final web app.
 - [model](/model.h5) This file contains the trained model.
 - [Emotion Detection](./Emotion%20Detection) This folder contains python scripts to train the model.
 - [.streamlit](./.streamlit) This folder contains configuration files for the streamlit theme in Web App.




### Future Scope
- Deploying the web app.
- Integration of an inbuilt music player using  SpotiPy library, with spotify authentication.
- Addition of more gestures, and control of volume using gesture detection.
- Improved Reliablity and addition of User Feedback 

### References
- [Emotional Detection and Music Recommendation System
based on User Facial Expression - S Metilda Florence and M Uma](https://iopscience.iop.org/article/10.1088/1757-899X/912/6/062007/pdf)


