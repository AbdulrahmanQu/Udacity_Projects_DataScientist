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
<br>
<a href = 'https://ikhlestov.github.io/pages/machine-learning/pytorch-notes/' >Pytorch Notes</a>
<br>
<a href = ' https://arxiv.org/pdf/1609.08764.pdf' > Data Augmentation </a>
<br>
<a href = 'https://machinelearningmastery.com/transfer-learning-for-deep-learning/'> Transfer Learning_1 </a>
<br>
<a href = 'http://cs231n.github.io/transfer-learning/'>Transfer Learning_2 </a>

Specific to this flower classification problem:

<br>
<a href= 'https://arxiv.org/ftp/arxiv/papers/1708/1708.03763.pdf' >Flower Classication_1 </a>
<br>
<a href = 'https://www.robots.ox.ac.uk/~vgg/research/flowers_demo/docs/Chai11.pdf' > Flower Classication_2</a>
