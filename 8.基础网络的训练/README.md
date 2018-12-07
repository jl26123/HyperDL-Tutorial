#### 基础网络的训练

目前我们常用的神经网络，github上基本都具有较为丰富的训练、测试代码，我们这里选择几种常用，高效的网络推荐给大家，包括与之对应的github工程，涉及一些训练的技巧，旨在让大家能够复现出作者原始的精度。

我们这里主要介绍以下几个网络的训练与使用:

```
1.MobileNet(分类网络)

2.MnasNet(分类网络)

3.MTCNN(单一物体检测网络)

4.MobileNet-SSD(Single Shot 物体检测网络)

5.ArcFace(人脸识别网络)

6.insightface(人脸识别网络)

7.VanillaCNN(人脸回归网络)

8.YOLO-V3(通用物体检测网络)

9.DeepOCR(文字识别网络)

```

以上这些网络涵盖了日常使用网络设计到的大部分功能，一些相关的应用也可以通过这些网络的变通，修改进行试验。

#### 1.MobileNet

MobileNet是谷歌发布的第一代专为移动端设计的高效网络，其后续版本MobileNet-v2同样优秀，shicai yang大神已经给出了网络的pretrain model，以及caffe的[训练、测试代码](https://github.com/shicai/MobileNet-Caffe)，利用该网络可以训练其他类似的分类任务，例如我们开源的[鉴黄网络](https://github.com/zeusees/HyperNSFW).

#### 2.MnasNet

MnasNet同样是谷歌发布的高效移动端分类网络，与Mobilenet不同之处在于网络的设计借助deepmind AI的能力，不是hand craft手动设计的网络，相比于mobilenet，速度快大约1.5倍，准确度提高将近两个点。我们同样复现了该网络，并且提供了该网络再标准ImageNet上的pretrain model，接近了官方的精度。连接地址：https://github.com/zeusees/Mnasnet-Pretrained-Model

#### 3.MTCNN

#### 4.MobileNet-SSD

#### 5.ArcFace

#### 6.insightface

#### 7.VanillaCNN

#### 8.YOLO-V3

通用物体检测近年来也是研究人员关注的人们领域，从RBG、何凯明大神的RCNN，Fast RCNN，Faster RCNN，MASK RCNN等，Single Shot的Yolo系列、SSD等，以后后来的RetinaNet，我们对这一系列的网络都进行过测试，由于我们算法组在日常使用中主要考虑移动端的部署以及服务器端的效率，推荐了MobileNet-SSD跟YOLO-V
3。我们对3000张行车记录仪标注图像以及2000张交通监控图片进行标注，分别在以上网络进行了测试，对于我们的图片，YOLO-V3表现最好，速度也基本是最快的。项目主页：https://pjreddie.com/darknet/yolo/ 













