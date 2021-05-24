[![forthebadge](https://forthebadge.com/images/badges/check-it-out.svg)](https://forthebadge.com)<br>
[![forthebadge](https://forthebadge.com/images/badges/built-with-love.svg)](https://forthebadge.com)<br>
[![forthebadge](https://forthebadge.com/images/badges/made-with-python.svg)](https://forthebadge.com)

# EYE CONTROLLED KEYBOARD : 

It is a eye-controlled keyboard for physically-challenged people. 
It uses Neural Networks to predict the eye's state accurately using which the virtual keybaord shown on the screen is operated.


![Alt text](demo.gif)

# How it works
For each frame in a second:
1. Using Dlib frontal face detector all of the 68 facial landmarks co-ordinates are detected and the co-ordinates are converted into numpy array.
2. Pass 36,37,38,39,40,41th index of array to the ```crop_eye()```
function as it contains co-ordinates of respective landmarks and function returns cropped image for left eye.
3. Similarly pass 42,43,44,45,46,47 index to get cropped image of right eye.
<br>
<img src="FILES\crop.png">
4.The cropped eyes images are passed to the two model blink detection model and gaze detection model. Blink detection model predicts the openning percentage of the eyes and gaze detection model predict the gaze of the eyes ie. either user is loking left, right or center<br>
5.Eyes blink is used to enter inside the particular column of the keyboard and Eyes gaze is used to shift the active column of the keyboard.

# For the more details read the paper on this project from [HERE](https://drive.google.com/file/d/1gniRFHjCecArHWOHneltp6tUWql5MirM/view?usp=sharing)

# For the dataset email me 

This code was developed on: 
```
python == 3.7.0
opencv-python == 4.3.0.36
tensorflow==2.3.0
dlib == 19.20.0
imutils==0.5.3
```

# NOTE:
 Download the shape_predictor_68_face_landmarks.dat file from [HERE](https://drive.google.com/drive/folders/1sBn-qxZW-cJC8epR0z63Kz3uwnS8SjZF?usp=sharing) and paste it in the Files folder. 

### With the joint effort of: https://github.com/R4j4n

![visitors](https://visitor-badge.glitch.me/badge?page_id=page.https://github.com/R4j4n/Neural-Keyboard)
