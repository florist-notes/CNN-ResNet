# CNN-ResNet
🕵🏻 Vision : Model 5: ResNet : Image Classification

<b>Paper</b> : ["Deep Residual Learning for Image Recognition"](https://arxiv.org/abs/1512.03385), <b>Talk</b> : [CVPR 2016](https://youtu.be/C6tLw-rPQ2o),

2015 [ILSVRC](http://www.image-net.org/challenges/LSVRC/) ([ImageNet](http://www.image-net.org/) Large-Scale Visual Recognition Challenge) <b>Winner</b> in all the three categories - classification, localization & detection.

It is a benchmark competition where teams across the world compete to classify, localize, detect ... images of 1000 categories, taken from the imagenet dataset.The imagenet dataset holds 15M images of 22K categories but for this contest: 1.2M images in 1K categories were chosen.The ILSVRC 2015 classification challenge involves the task of classifying the image into one of 1000 leaf-node categories in the Imagenet hierarchy. There are about 1.2 million images for training, 50,000 for validation and 100,000 images for testing. Each image is associated with one ground truth category, and performance is measured based on the highest scoring classifier predictions. Two numbers are usually reported: the top-1 accuracy rate, which compares the ground truth against the first predicted class, and the top-5 error rate, which compares the ground truth against the first 5 predicted classes: an image is deemed correctly classified if the ground truth is among the top-5, regardless of its rank in them. The challenge uses the top-5 error rate for ranking purposes. Team " MSRA ", achieved top 5 test error rate of 3.6%, It was way too good. Check ILSVRC 2015 [results](http://image-net.org/challenges/LSVRC/2015/results).

This paper is important as it is the first paper which brought down the computer vision error rate ( 3.6% achieved) below human level error of 5-10%. What it meant was that, computers are now less error prone than humans in classifying objects in an image. Several experiments were done to measure human error rate, one of the most famous experiment is covered in [Andrej Karpathy's blog](http://karpathy.github.io/2014/09/02/what-i-learned-from-competing-against-a-convnet-on-imagenet/) on "Experiences with competing against ConvNets on the ImageNet challenge".

<img src="https://github.com/SKKSaikia/CNN-ResNet/blob/master/img/ResNet.gif">

Overview
-
ResNet is a Deep Network proposed by [Kaiming He](http://kaiminghe.com/), [Xiangyu Zhang](https://www.cs.purdue.edu/homes/xyzhang/), [Shaoqing Ren](http://shaoqingren.com/) and [Jian Sun](http://www.jiansun.org/) from <b>Microsoft Research Asia.</b>


Architecture
-
<img src="https://github.com/SKKSaikia/CNN-ResNet/blob/master/img/comp.png">

We can see that the ResNet architecture is made up of repeated loop kind of blocks with 2 convolutional layer within. This block is called the <b>"Residual block"</b>. A general notion of a residual block can be visualized as,

<img src="https://github.com/SKKSaikia/CNN-ResNet/blob/master/img/res.png">

The idea behind a residual block is that you have your input x go through conv-relu-conv series. This will give you some F(x). That result is then added to the original input x. Let’s call that H(x) = F(x) + x. In traditional CNNs, your H(x) would just be equal to F(x) right? So, instead of just computing that transformation (straight from x to F(x)), we’re computing the term that you have to add, F(x), to your input, x. Basically, the residual block shown above is computing a “delta” or a slight change to the original input x to get a slightly altered representation (When we think of traditional CNNs, we go from x to F(x) which is a completely new representation that doesn’t keep any information about the original x). The authors believe that “it is easier to optimize the residual mapping than to optimize the original, unreferenced mapping”.

model.summary()
-

Important Points
-

Practical
-

Versions
-

    1. Layers - 50 / 101 / 152
    2. Deep Residual Network
    3. Wide Residual Network
    4. ResNeXt
