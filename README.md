# Pneumonia-Analysis-System-Based-on-CNN
Xiangnan Zhang <br/>
School of Future Technology, Beijing Institute of Technology
## Introduction
This Model realized a dicotomy between normal and pneumonia according to X-ray images. 
The classification accuracy is about 90% (in test dataset with 624 images). The TensorFlow subclassed model is saved as Model_1(SaveModel format). Source files including training programme and testing programme are in the folder Source_File.
## About File Directories
FolderName | Discription
-|-
Dataset/shuffled_csv | Contains 2 csv files, the index of training and testing data
Model_1 | model as SaveModel format
Source_file | contain sorce codes for training, testing and using
## Structure of the CNN Model
The structure are as follows:
### Unit 1: Convolution Unit
Layer | Discription
-|-
Conv2D | 16, size=5, ReLU
Conv2D | 16, size=5, ReLU
MaxPool2D | size=4
Dropout | ratio=0.2
### Unit 2: Convolution Unit
Layer | Discription
-|-
Conv2D | 32, size=5, ReLU
Conv2D | 32, size=5, ReLU
MaxPool2D | size=4
Dropout | ratio=0.2
### Unit 3: Dense Unit
Layer | Discription
-|-
Flatten |
Dense | 256, ReLU
Dense | 2, Softmax
## Data Preprosessing
While the size of images in the Dataset are not the same, as well as to maintain their features, all the images are resized as 1100*1100 befor being inputted into the model.
It seems like this:
![Image](https://img-blog.csdnimg.cn/direct/0efca1dc46014be494fedef06fa9aa7e.png) <br/>
> Notice: This is the output from the sorce file Predict(for user).ipynb.



