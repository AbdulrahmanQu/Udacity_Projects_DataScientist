[//]: # (Image Reference)

[image1]: ./images/output1.png "Sample Output"

# Dog-breed Classifier

## Project Overview

this project is a final project for Udacity's nano degree data scientist progrem, this project is a convolutional neural networks (CNN) , i learned how to build a pipeline that can be used within a web or mobile app to process real-world, user-supplied images. Given an image of a dog, though the algorithm it will identify an estimate of the canine’s breed. If supplied an image of a human, the code will identify the resembling dog breed.

![Sample Output][image1]

## Project Instruction

### Instructions

1. Clone the repository and navigate to the downloaded folder.
```    
git clone https://github.com/AbdulrahmanQu/Udacity_Projects_DataScientist.git
cd  Udacity_Projects_DataScientist/Dog Breed Capstone
```
2. Open the `dog_app.ipynb`
```
jupyter notebook - > dog_app.ipynb
=    ```
3. all the datasets are ready to be downloaded from the notebook, thus it may take hours to be fully ready with the files needed.

or

- Download the [dog dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/dogImages`. 

- Download the [human dataset](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/lfw.zip).  Unzip the folder and place it in the repo, at location `path/to/dog-project/lfw`.  
If you are using a Windows machine, you are encouraged to use [7zip](http://www.7-zip.org/) to extract the folder. 

- Donwload the [VGG-16 bottleneck features](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/DogVGG16Data.npz) for the dog dataset.  Place it in the repo, at location `path/to/dog-project/bottleneck_features`.


## Project Information

### Contents


- Step 0: Import Datasets
- Step 1: Detect Humans
- Step 2: Detect Dogs
- Step 3: Create a CNN to Classify Dog Breeds (from Scratch)
- Step 4: Use a CNN to Classify Dog Breeds (using Transfer Learning)
- Step 5: Create a CNN to Classify Dog Breeds (using Transfer Learning)
- Step 6: Write your Algorithm
- Step 7: Test Your Algorithm

### Main CNN Model
I had tried to imitate VGG-16 in the step 4 and I used Xception for the transfer learning in step 5

### Libraries

The list below represents main libraries and its objects for the project.
- [keras](https://keras.io/) (Convolutional Neural Network)
- [OpenCV](https://opencv.org/) (Human Face Detection)
- [Matplotlib](https://matplotlib.org/) (Plot Images)
- [Numpy](http://www.numpy.org/) (^^)
