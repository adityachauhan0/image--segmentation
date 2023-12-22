# SOTA- image segmentation
This project implements image segmentation with tensorflow2

## dataset preparation

download COCO2017 dataset from [here](https://cocodataset.org/). 

```python
python3 create_dataset.py </path/to/train2017> </path/to/val2017> </path/to/annotations>
```
use this to unzip the dataset to train2017, val2017 and annotations folder
there should also be trainset and testset generated after running this script.

## train with dataset

train with multithreaded processes (several GPU)

```python
python3 train_eager_distributed.py
```

train with only one GPU

```python
python3 train_eager.py
```

or 

```python
python3 train_keras.py
```

## save model

```python
python3 save_model.py
```

## how to predict with the saved (already trained) model

```python
python3 test.py </path/to/image>
```


