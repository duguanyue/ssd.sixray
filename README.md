# 目标检测——样本不均衡
在样本不均衡的情况下进行目标检测.

## 训练环境 
>  Python 3.7  
>  pytorch 1.3  
>  ssd

## 数据文件
训练数据集合将原数据集`core_500`和`coreless_5000`合并。  
请将训练数据合并后存储到`data/sixray/`目录，目录结构下：

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

## 训练
#### _运行_
在终端直接`python train.py`  
（注意自行调整参数，如`batch_size, max_iter`等）

#### _结果_
最终训练出的模型默认存储为`weights/SIXRAY.pth`

## 测试
在终端直接`python test.py`  
最终结果存储为`eval/test1.txt`
## 验证
在终端直接`python eval.py`  
最终结果存储在`eval/`
## 模型指标

| mAP    | core_AP | coreless_AP |
| ------ | ------- | ----------- |
| 0.99 |  0.99 | 0.99      |


## VGG16
SSD基于VGG16，请下载预训练模型文件到`weights/`.
[vgg16_reducedfc.pth](https://s3.amazonaws.com/amdegroot-models/)

# References

[pytorch-ssd](https://github.com/amdegroot/ssd.pytorch).  
Wei Liu, et al. "SSD: Single Shot MultiBox Detector." [ECCV2016](http://arxiv.org/abs/1512.02325).
