# Deep Learning Methods for Chest X-ray Classification

## Abstract
In this paper, we investigate several deep learning models for use
in diagnosing diseases from chest X-ray images. We train a simple
convolutional neural network (CNN), a ResNet model, a
DenseNet model, and an Extended CNN model on a subset of
images from the CheXpert dataset of chest X-ray images, both for
binary classification of pneumonia and multi-label classification
of multiple pathologies. Our Extended CNN model is based on
our Simple CNN model but includes features that are not
commonly used in X-ray classification, namely multiple image
views and electronic health record (EHR) data. Our goal is to see
whether these additional features can give researchers another
option in which to improve their models. In this study we
evaluate the results of our Extended CNN model using accuracy,
AUC, and F1 score and compare to our Simple CNN model as the
baseline and also to the state-of-the-art models developed by other
researchers. Both the ResNet and DenseNet were modified for our
needs and did not use pre-trained weights. We find that we are
able to achieve and replicate similar performance using these
state-of-the-art models with our dataset. The results from our
Extended CNN model fell short of those of the state of the art
models, however with some modifications we believe there could
be some merit with the framework  

The full paper in pdf format can be found [here](https://steve303.github.io/DeepLearning-XrayClassify/CS598_XrayClassifyPaper.pdf)  
A summary in pptx format can be found [here](https://steve303.github.io/DeepLearning-XrayClassify/CS598_XrayClassify.pptx)

## Data
Example data and structure is found in the `/images/` file - this is a drastically reduced dataset from the original CheXpert dataset, to be used to *validate only that the provided code runs (specifically the below csvs will work for the multi-label simple CNN/ResNet/DenseNet models).*
- `/images/restricted_example_train.csv` - csv limited to 64 patients with corresponding images available in the `/images/CheXpert-v.10-small/train` folder
- `/images/restricted_example_valid.csv` - csv limited to 50 patients with corresponding images available in the `/images/CheXpert-v1.0-small/valid` folder

Data was obtained from the [CheXpert Dataset](https://stanfordmlgroup.github.io/competitions/chexpert/) based on the paper [CheXpert: A Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison](https://arxiv.org/abs/1901.07031). 
The code uses the `test.csv` and `valid.csv` files to pull the images, so these files can be modified and restricted to the available images for training/testing. 

## Models
The model building code is found in the `/Models/` file.

- Binary Simple CNN: `Pneumonia_SimpleCNN.ipynb`
- Binary Extended CNN: `Pneumonia_ExtendedCNN.ipynb`
- Binary ResNet18: `Pneumonia_ResNet.ipynb`
- Binary DenseNet121: `Pneumonia_DenseNet.ipynb`
- Multi-label Simple CNN: `Multilabel_SimpleCNN.ipynb`
- Multi-label Extended CNN: `Multilabel_ExtendedCNN.ipynb`
- Multi-label ResNet18: `Multilabel_ResNet.ipynb`
- Multi-label DenseNet121: `Multilabel_DenseNet.ipynb`

## Training and Testing
The models were run on [Google Colab](https://colab.research.google.com/) attached to a Google Drive folder containing the CheXpert dataset. 
To reference the appropriate data, set the values of the following variables:
```
IMG_PATH =  #input your image path here
TRAIN_CSV = #input your train.csv file path here
VALID_CSV = #input your valid.csv file path here
```

