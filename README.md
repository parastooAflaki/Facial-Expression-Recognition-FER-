# Facial-Expression-Recognition
This is the final project of Computer vision course fall 2020 by [Professor Alireza Talebpour](http://facultymembers.sbu.ac.ir/talebpour/). 

---

## Description

Emotion recognition is the process of identifying human emotion, most typically from facial expressions as well as from verbal expressions.

We implemented two deep learning models for facial expression recognition (FER) using FER2013 dataset for recognizing 6 emotion of (Anger ,Disgust, Fear, Happy, Sad, 
Surprise, Neutral).

### Dataset

FER2013 dataset consists of 35,887 Gray Scale images with 48x48 resolution. This dataset was created by gathering the results of a Google image search of each emotion and synonyms​ ​of​ ​the​ ​emotions. 
  * Include face occlusion,partial faces, low-contrast images, and eyeglasses
  ![image](https://user-images.githubusercontent.com/47450201/152584888-9cb081ce-fb0f-4610-a7ca-eb047f9132e4.png)

  * Includes Seven emotions: happy, sad, angry, afraid, surprise, disgust, and neutral


### Preprocessing
Pre-processing is required to align and normalize the visual semantic information conveyed by the face.

We applied multiple preprocessing technique before spliting data and training models.
* Apply noise reduction : Detect the face and remove background and non-face areas
* Augmentation : Flip, Rotation, Scale, Crop, Translation and Affine transformation
* Edge detection 

### First Model(paper model)
This model is based on the CNN introduced in paper, [Deep-Emotion](https://arxiv.org/abs/1902.01019)
* Architecture

<p align="center">
  <img src="img/result1.png" width="500" title="Architecture">
</p>

* Result

| Training Accuracy  | Validation Accuracy | Test Accuracy |
| ------------- | ------------- | ------------- |
| 87% | 67%  | 58% |


### Second Model(miniVGG)
This model is modified version of VGG.
* Architecture

<p align="center">
  <img src="img/result2.png" width="500" title=" Architecture">
</p>

* Result


| Training Accuracy  | Validation Accuracy | Test Accuracy |
| ------------- | ------------- | ------------- |
| 75% | 61%  | 61% |
