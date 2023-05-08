## Diagnosing Respiratory Disease from Chest X-Rays using Computer Vision

## Problem
We seek to classify common respiratory diseases (viral pneumonia, lung opacity, COVID, and normal) from chest x-ray images via a survey of supervised and self-supervised methods. 

## Approach
![Screenshot](screenshot.png)


## Structure
As different individuals worked on the various approaches, each of the notebooks under ```models``` is self-sustained. We have also provided a ```requirements.txt``` which contains all of the necessary dependencies. Each of the models can be run on Google Colab. While the CNN models (ResNet18 and VGG16) can train on a cpu, EVAE and MAE require a gpu for training.
```
diagnosing_respiratory_disease_cv
│   README.md
└───requirements.txt
└───models
│   └───resnet_vgg.ipynb
│   └───evae.ipynb
│   └───mae_vit.ipynb
```

