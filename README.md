# CIFAR-10
## Introduction
The CIFAR-10 dataset (Canadian Institute For Advanced Research) is a collection of images that are commonly used to train machine learning and computer vision algorithms. It is one of the most widely used datasets for machine learning research. The CIFAR-10 dataset contains 60,000 32x32 color images in 10 different classes. The 10 different classes represent airplanes, cars, birds, cats, deer, dogs, frogs, horses, ships, and trucks. There are 6,000 images of each class.


![image](https://user-images.githubusercontent.com/67097978/169860407-8074c31b-4fd8-4111-ac43-90bcc00d33f7.png)


## Prerequisites
- **Python** 3.7.13
- **PyTorch** 1.11.0
- **Torchvision** 0.12.0
- **CUDA** 11.2
- **NumPy** 1.21.6
- **Matplotlib** 3.2.2

## Usage
We implement our code on Jupyter Notebook, and run it on Google Colab. <br />
Details about the CIFAR-10 dataset could be found at: https://www.cs.toronto.edu/~kriz/cifar.html

#### Optimization Strategies:
- Data Augmentation
- Tuning hyperparameters
- Using a more sophisticated CNN such as GoogLeNet

#### The optimized hyperparameters we used:
- **Learning rate:** 0.001
- **Batch size:** 4
- **Epochs:** 10
- **Criterion:** CrossEntropy
- **Optimizer:** SGD

#### Structure of the repo:
```
├── models/
│   ├── LeNet.py
│   ├── AlexNet.py
│   ├── VGGNet.py
│   └── GoogLeNet.py
├── Initial_CNN.ipynb
├── Optimized_CNN.ipynb
├── README.md
```
- `Initial_CNN.ipynb` is the realization of the CNN with fairly poor accuracy (60.74%).
- `Optimized_CNN.ipynb` is the realization of the CNN after optimization, using GoogLeNet (86.13%).

## Results
The following were the accuracy on the test set as well as the training time of different models: 
Models | Accuracy (%) | Training Time (s)
:---:|:---: | :---:
[LeNet](https://github.com/IvoryCandy/pytorch-cifar10/blob/master/models/LeNet.py) | 65.37 | 596.99
[Alexnet](https://github.com/IvoryCandy/pytorch-cifar10/blob/master/models/AlexNet.py) | 76.36 | 1420.02
[VGG11](https://github.com/IvoryCandy/pytorch-cifar10/blob/master/models/VGG.py) | 81.89 | 1200.45
[VGG13](https://github.com/IvoryCandy/pytorch-cifar10/blob/master/models/VGG.py) | 83.48 | 1359.55
[GoogleNet](https://github.com/IvoryCandy/pytorch-cifar10/blob/master/models/GoogleNet.py) | 86.13 | 6113.05

 <br />Here are the loss and accuracy varying to the epoch on the training set:

![image](https://user-images.githubusercontent.com/67097978/169862338-415273a2-a1fd-406e-8f0f-786baeb36cfd.png)

![image](https://user-images.githubusercontent.com/67097978/169862362-dbe7cfa7-df31-4a87-a79f-02f68b50ec85.png)

