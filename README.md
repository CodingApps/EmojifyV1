
<h1 align="center"> Emojify </h1> <br>

<h4 align="center"> Take picture and use Google Face API to detect faces, then apply images. </h4> <br>
 

## Intro

This project implements the Google Face API for face recognition after a picture is taken. Once the face recognition detects the facial expression, another function pulls a cartoon emoji with the corresponding expression to place on the face.
<p align="center">
  <img alt="emojify" title="emojify" src="http://androidflow.github.io/screens/emojifypic1.gif" width=300>
</p>
<br>

## Functions 

* Detect face with Google Face API.
* Assign image based on results from API.  
* Select picture from image index and overlay on face within photo. 
<br>

## Determining Placement of Emoji

After selecting the Emoji, it had to be determined where on the photo to place it. With the values returned from the API, the placement could be calculated to estimate the coordinates.  
``` java
       float emojiPositionX =
                (face.getPosition().x + face.getWidth() / 2) - emojiBitmap.getWidth() / 2;
       float emojiPositionY =
                (face.getPosition().y + face.getHeight() / 2) - emojiBitmap.getHeight() / 3;
```
<br>

