# AI image classification and machine learning utilizing the PyTorch framework

Project assets:

- `Image Classifier Project.ipynb` Jupyter Notebook
- `Image Classifier Project.html` HTML export of the Jupyter Notebook above.
- `train.py` to train a new network on a data set.
- `predict.py` to predict flower name from an image.

## Example Image for Training


Get flower images:
```bash
mkdir -p flowers && cd flowers
curl https://s3.amazonaws.com/content.udacity-data.com/nd089/flower_data.tar.gz | tar xz
```

You should now have **test**, **train** and **valid** directories containing classification directories and flower images under the **flowers** directory.

## Examples



Train on **GPU** with **densenet121** with one **500** node layer:
```bash
python train.py ./flowers/train --gpu --arch "densenet121" --hidden_units 500
```


Basic Prediction
```bash
python predict.py ./flowers/valid/5/image_05192.jpg ./checkpoint.pth
```

Prediction with GPU
```bash
python ./predict.py ./flowers/valid/5/image_05192.jpg ./checkpoint.pth --gpu
```


[flower_data.tar.gz]:https://s3.amazonaws.com/content.udacity-data.com/nd089/flower_data.tar.gz

---------------------------------------

Review:

Meets Specifications
Great work!
Congratulations on completing your project!
I certainly enjoyed walking though your code. It's very clean and very well commented. I can clearly see the effort that has been put into this.
I tried the command line utility too, it works like a charm! Very well implemented.
Here are some addition links that might help you further your understanding:

<a href = 'https://ikhlestov.github.io/pages/machine-learning/pytorch-notes/' >Pytorch Notes</a>
<a href = ' https://arxiv.org/pdf/1609.08764.pdf' > Data Augmentation </a>
<a href = 'https://machinelearningmastery.com/transfer-learning-for-deep-learning/'> Transfer Learning_1 </a>
<a href = 'http://cs231n.github.io/transfer-learning/'>Transfer Learning_2 </a>

Specific to this flower classification problem:

<a href= 'https://arxiv.org/ftp/arxiv/papers/1708/1708.03763.pdf' >Flower Classication_1 </a>
<a href = 'https://www.robots.ox.ac.uk/~vgg/research/flowers_demo/docs/Chai11.pdf' > Flower Classication_2</a>

Files Submitted
The submission includes all required files. (Model checkpoints not required.)

All the required files are included.

Part 1 - Development Notebook
All the necessary packages and modules are imported in the first cell of the notebook

Moving all the imports to the top is just a good practice as it helps in looking at the dependencies and the import requirements of the project in one go.

torchvision transforms are used to augment the training data with random scaling, rotations, mirroring, and/or cropping

The training, validation, and testing data is appropriately cropped and normalized

The data for each set (train, validation, test) is loaded with torchvision's ImageFolder

The data for each set is loaded with torchvision's DataLoader

A pretrained network such as VGG16 is loaded from torchvision.models and the parameters are frozen

A new feedforward network is defined for use as a classifier using the features as input

The parameters of the feedforward classifier are appropriately trained, while the parameters of the feature network are left static

During training, the validation loss and accuracy are displayed

The network's accuracy is measured on the test data

There is a function that successfully loads a checkpoint and rebuilds the model

The trained model is saved as a checkpoint along with associated hyperparameters and the class_to_idx dictionary

The process_image function successfully converts a PIL image into an object that can be used as input to a trained model

The predict function successfully takes the path to an image and a checkpoint, then returns the top K most probably classes for that image

A matplotlib figure is created displaying an image and its associated top 5 most probable classes with actual flower names

Part 2 - Command Line Application
train.py successfully trains a new network on a dataset of images and saves the model to a checkpoint

The training loss, validation loss, and validation accuracy are printed out as a network trains

The training script allows users to choose from at least two different architectures available from torchvision.models

The training script allows users to set hyperparameters for learning rate, number of hidden units, and training epochs

The training script allows users to choose training the model on a GPU

The predict.py script successfully reads in an image and a checkpoint then prints the most likely image class and it's associated probability

Yes, I can't get the error this time around.

The predict.py script allows users to print out the top K classes along with associated probabilities

Yes, it does! Tried it with varying values of K and it works like a charm.
The predict.py script allows users to load a JSON file that maps the class values to other category names

The predict.py script allows users to use the GPU to calculate the predictions
