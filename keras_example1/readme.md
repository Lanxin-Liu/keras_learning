# 一般优化的方法
1. 一些功能强大的 CNN 体系架构
    -- mnist集有使用CNN进行训练的模型，可以达到较好的效果。对于本例判断两个数字是否为同一个，是否可以使用CNN网络？(https://dataxujing.github.io/%E7%94%A8CNN%E5%AE%9E%E7%8E%B0MNIST%E6%95%B0%E6%8D%AE%E9%9B%86/)
2. 使用较小的学习率
3. 使用dropout
4. 修改输出层
    -- 使用适合的领域的新激活函数和输出大小替换模型默认值。
# 降低过拟合的方法
1. 简化模型 (非线性模型->线性模型)
2. 添加约束项以缩小假设空间 （L1、L2正则化）
3. 集成学习
4. Dropout超参数
5. 通过空间变化、颜色变化等方式扩充数据

# 本例详解
1. keras识别mnist手写数据集：https://github.com/Gary-Deeplearning/Keras-Tutorial/blob/master/part1-First-Nerual-Network.py
1. siamese网络：https://blog.csdn.net/sxf1061926959/article/details/54836696
2. keras实现siamese网络：https://github.com/Gary-Deeplearning/Keras-Tutorial/blob/master/Siamese.py
# 优化
1. 问题分析：
    1. 训练集准确率略高于测试集
2. 可能有优化(待验证)
    1. https://github.com/Shicoder/DeepLearning_Demo/tree/master/siamese_tf_mnist
    2. Hamming Distance Metric Learning(https://github.com/norouzi/hdml)
    3. Learning to Compare Image Patches via Convolutional Neural Networks
3. mnist_siamese1~5是与siamese网络相关的一些方法，在结果上可能并没有做到优化。
    -- mnist_siamese1~4的准确率较原版没有太大的改变在97.4%上下浮动，mnist_siamese5的准确率较低在93%上下浮动
