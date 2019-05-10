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
