# 目标检测——样本不均衡
Big Homework about charger recognition.

## 环境 
>  python3  
>  pytorch  
>  ssd

## 运行方式
在终端直接`python train.py --cuda False`  
或直接运行 `./run.sh`


## 数据文件
训练数据集合将原数据集`core_500`和`coreless_5000`合并。  
请将训练数据合并后存储到`./data/sixray/`目录，目录结构下：

```
.
`-- sixray
    |-- Annotation
    |   |-- core_battery00000003.txt
    |   |-- core_battery00000004.txt
    |   |-- coreless_battery00000053.txt
    |   `-- ...
    |-- Image
    |   |-- core_battery00000003.jpg
    |   |-- core_battery00000004.jpg 
    |   |-- coreless_battery00000053.jpg
    |   `-- ...
    |-- core_500.txt
    |-- coreless_5000.txt
    |-- all5500.txt
    |-- train_3850.txt
    `-- test_1650.txt
```
## 结果
最终训练出的模型存储为`./weights/SIXRAY.pth`

## VGG16
SSD基于VGG16，请下载预训练模型文件到`./weights/`。
[vgg16_reducedfc.pth](https://s3.amazonaws.com/amdegroot-models/)
