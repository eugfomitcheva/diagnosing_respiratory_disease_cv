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
└───data
│   └───data_origination.ipynb
└───models
│   └───baseline_models.ipynb
│   └───resnet_vgg.ipynb
│   └───evae.ipynb
│   └───mae_vit.ipynb
└───ignore
```

## Instructions For Use
1. baseline_models.ipynb
- Set the path to the COVID-19 Radiography Dataset in the first code block under section 1. Read / Format Data.
    - The pathway should include everything except the name of the folder where the data is stored
    - An example of a correctly formatted data path is given in the notebook.

2. resnet_vgg.ipynb
- Select the desired options for classification task, model type, and training task
    - Classification options: ['multiclass', 'binary']
    - Model options: ['resnet', 'vgg']
    - Training options: ['finetune', 'scratch']
- Format data into folders consisting of train/val/test splits
    - In the notebook, this folder is called 'train_val_test', and contains a 60:30:10 split for all raw images for each class

3. evae.ipynb
- Amend pathfiles to data
- Requires pre-trained ResNet18 and VGG16 (loads in saved weights)
    - Revision of filepaths for these models is sufficient for implementation to run
- Training recommended on GPU; depending on performance 20 epochs can take 3+ hours
    
4. mae_vit.ipynb
- Amend pathfiles to data
- Training recommended on GPU; depending on performance 20 epochs can take 3+ hours
