# YFtensorflow
1. 关于TensorFlow安装，请参考[【TensorFlow】Windows10 64 位下安装 TensorFlow - 官方原生支持](https://blog.csdn.net/u010099080/article/details/53418159)
2. 先安装集成环境Anaconda（不会覆盖之前安装的python3.6）.我使用的是3.6版本。
3. 然后pip -3 -m install tensorflow-gpu，建议安装gpu版本，通过pip安装cpu版本编译效率很低。我使用的是1.7版本。
4. 安装cuda,我先安装官网推荐的版本：CUDA9.1。运行提示找不到某个**90**dll文件。然后百度cuda9.0下载安装，会有警告，可以安装多个不同版本。把该dll文件路径添加环境变量。我的路径：C:\Program Files\NVIDIA GPU Computing Toolkit\CUDA\v9.0\extras\CUPTI\libx64
5. 安装cuDNN，解压放到任何一个目录下就行，然后把其中的bin目录路径添加到Path环境变量里。
3. MNIST数据集下载。下载脚本input_data.py，[地址](https://github.com/tensorflow/tensorflow/tree/master/tensorflow/examples/tutorials/mnist)。
使用时新建test.py文件（与input_data.py在同一工程目录下），执行下面命令来下载MNIST数据集，就会在mnist文件夹下生成一个data文件夹
```
#下载用于训练和测试的mnist数据集的源码

import input_data # 调用input_data
mnist = input_data.read_data_sets('data/', one_hot=True)
```