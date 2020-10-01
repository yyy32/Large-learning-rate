# Large-learning-rate

##  Computer vision:
### Installations
* pytorch : ``` pip install pytorch```
* torchvision : ``` pip install torchvision```

### dataset
* cifar10
* cifar100
* imagenet32: download the imagenet32 (http://image-net.org/download-images)

You can use generate a folder to store dataset :  ``` data/cifar10```,  ``` data/cifar100```,  ``` data/imagenet32```

### training
```
python largelearningrate/image_classification/train.py --epochs 120 --lr 0.1 --opt sgdm --gpu 0 --dataset imagenet32
```
or
```
python largelearningrate/image_classification/train.py --epochs 120 --lr 1.1 --opt sgd --gpu 0 --dataset imagenet32
```

You can select different optimizers and models with same parameters as : ```The paper : The simpler the better: vanilla SGD revisited```

### test

we have uploaded the sgd and sgdm model on imagenet32, you can test immediately.

## Speech Recognition:

### Installations
* pytorch : ``` pip install pytorch```
* librosa : ``` pip install librosa```

### dataset
* Google Commands Dataset: download the dataset (https://ai.googleblog.com/2017/08/launching-speech-commands-dataset.html)

You can generate a folder to store dataset :  ``` data/gcommands```

### training
```
python largelearningrate/gcommands/run.py --optimizer sgdm --lr 0.01 --epochs 150 
```
or 
```
python largelearningrate/gcommands/run.py --optimizer sgd --lr 0.15 --epochs 150 
```

## LSTM language model:

### Installations
* pytorch : ``` pip install pytorch```

### dataset
* Penn Treebank


### training

cd largelearningrate/lstm
```
python main.py --batch_size 20 --data data/penn --dropouti 0.4 --dropouth 0.25 --seed 11 --epoch 150 --nlayers 3 --optimizer sgd --lr 30 --gpu 1
```
or 
```
python main.py --batch_size 20 --data data/penn --dropouti 0.4 --dropouth 0.25 --seed 11 --epoch 150 --nlayers 3 --optimizer sgdm --lr 1 --gpu 1
```



