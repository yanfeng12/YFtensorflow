# YFtensorflow
1. 关于TensorFlow安装，请参考[【TensorFlow】Windows10 64 位下安装 TensorFlow - 官方原生支持](https://blog.csdn.net/u010099080/article/details/53418159)
2. MNIST数据集下载。下载脚本input_data.py，[地址](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/examples/tutorials/mnist)。
使用时新建test.py文件（与input_data.py在同一工程目录下），执行下面命令来下载MNIST数据集，就会在mnist文件夹下生成一个data文件夹
```
#下载用于训练和测试的mnist数据集的源码

import input_data # 调用input_data
mnist = input_data.read_data_sets('data/', one_hot=True)
```