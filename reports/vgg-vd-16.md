### Report for vgg-vd-16
Model params 528 MB 

Estimates for a single full pass of model at input size 224 x 224: 

* Memory required for features: 58 MB 
* Flops: 16 GFLOPs 

Estimates are given below of the burden of computing the `pool5` features in the network for different input sizes using a batch size of 128: 

| input size | feature size | feature memory | flops | 
|------------|--------------|----------------|-------| 
| 112 x 112 | 4 x 4 x 512 | 2 GB | 493 GFLOPs |
| 224 x 224 | 7 x 7 x 512 | 7 GB | 2 TFLOPs |
| 336 x 336 | 11 x 11 x 512 | 16 GB | 4 TFLOPs |
| 448 x 448 | 14 x 14 x 512 | 29 GB | 8 TFLOPs |
| 560 x 560 | 18 x 18 x 512 | 45 GB | 12 TFLOPs |
| 672 x 672 | 21 x 21 x 512 | 65 GB | 18 TFLOPs |

A rough outline of where in the network memory is allocated to parameters and features and where the greatest computational cost lies is shown below.  The x-axis does not show labels (it becomes hard to read for networks containing hundreds of layers) - it should be interpreted as depicting increasing depth from left to right.  The goal is simply to give some idea of the overall profile of the model: 

![vgg-vd-16 profile](figs/vgg-vd-16.png)
