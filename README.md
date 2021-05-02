# CS598-DL4H-Chest-X-ray-Classification
Chest X-ray classification using the CheXpert dataset as part of the final paper for CS598 Deep Learning for Healthcare

## Paper
The full paper can be found in `paper.pdf`

## Data
Example data and structure is found in the `/images/` file - this is a drastically reduced dataset from the original CheXpert dataset, to be used to *validate only that the provided code runs (specifically the below csvs will work for the multi-label simple CNN/ResNet/DenseNet models).*
- `/images/restricted_example_train.csv` - csv limited to 64 patients with corresponding images available in the `/images/CheXpert-v.10-small/train` folder
- `/images/restricted_example_valid.csv` - csv limited to 50 patients with corresponding images available in the `/images/CheXpert-v1.0-small/valid` folder

Data was obtained from the [CheXpert Dataset](https://stanfordmlgroup.github.io/competitions/chexpert/) based on the paper [CheXpert: A Large Chest Radiograph Dataset with Uncertainty Labels and Expert Comparison](https://arxiv.org/abs/1901.07031). 
The code uses the `test.csv` and `valid.csv` files to pull the images, so these files can be modified and restricted to the available images for training/testing. 

## Models
The models are found in the `/Models/` file.

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
