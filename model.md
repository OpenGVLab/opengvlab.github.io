## Common Setting 

* All checkpoints are distilled based on the feature of `INTERN MN-B15`. `Classification`, `Detection`, and `Segmentation` are distilled at the same time. 
* We use distributed pytorch for training, distillation, and validation. 
* The accuracy provided in the model zoo is the accuracy of finetune on the `ImageNet` dataset. 
* We use the `count_params` and `count_flops` from [utils.py](#TBD) to calculate the amount of parameters and FLOPS. 

## Model Structure

* [ResNet](#resnet), [Deep Residual Learning for Image Recognition](https://arxiv.org/abs/1512.03385)
* [MetaNet](#metanet), [coming soon](####metanet)
* [MobileNet-v2](#mobilenet-v2), [MobileNetV2: Inverted Residuals and Linear Bottlenecks](https://arxiv.org/abs/1801.04381)
* [ViT](#Vision_Transformer), [An Image is Worth 16x16 Words: Transformers for Image Recognition at Scale](https://arxiv.org/abs/2010.11929)
* [EfficientNet](#EfficientNet), [EfficientNet: Rethinking Model Scaling for Convolutional Neural Networks](https://arxiv.org/pdf/1905.11946.pdf)
* [Swin Transformer](#Swin_Transformer), [Swin Transformer: Hierarchical Vision Transformer using Shifted Windows](https://arxiv.org/abs/2103.14030)

## Model Benchmark

Models and  benchmarks can apply for [opengvlab_modelzoo](#TBD)'s access. 

#### ResNet

| Model         | Description | Params (M)    | FLOPs (G)     | Top-1         | T4-fp32(ms) | T4-fp16(ms) | T4-int8(ms) |
| ---           | ---                             | ---           | ---           | ---           | ---           | ---           | ---           |
| ResNet-18     |      | 11.7          | 1.813         | 69.8        | 1.36557 | 0.548359 | 0.392792 |
|               | Distilled from S3.MN-B15  | 11.7          | 1.813         | 72.04        |         |         |         |
| ResNet-34 |   | 21.8 | 3.67 | 74.16 | 2.47336 | 0.959072 | 0.714086 |
|  | Distilled from S3.MN-B15  | 21.8 | 3.67 | 74.17 |  |  |  |
| ResNet-50     |      | --- | 25.5          | 4.087         | 76.8        | 3.47636 | 1.12056 | 0.856407 |
|               | Distilled from S3.MN-B15  | 25.5          | 4.087         | 78.8      |       |       |       |
| ResNet-101    |     | 45.6   | 15.5             | 77.4          | 6.37888 | 2.04407   | 1.61156 |
|               | Pretrained on JFT-300M  | 45.6   | 15.5             | 79.2           |            |            |            |
|               | Distilled from S3.MN-B15  | 45.6   | 15.5             | **81.3**           |            |            |            |

#### MetaNet

| Model         | Description              | Params (M)    | FLOPs (G)     | Top-1         | fp32(ms) | fp16(ms) | int8(ms) |
| ---           | ---                      | ---           | ---           | ---           | ---           | ---           | ---           |
| MN-B4         |            | 31.7M   | 3.17              | 77.4          | 7.64342 | 6.95379 | 6.49423 |
|               | Distilled from S3.MN-B15       | 31.7M   | 3.17              | 82.2          |           |           |           |
| MN-B7         |  | 100.2M   | 7.26             | 77.4             | 12.749 | 9.74931 | 11.7695 |
|               | Distilled from S3.MN-B15  | 100.2M   | 7.26             | 84.8           |            |            |            |


#### MobileNet-v2

| Model         | Description                 | Params (M)    | FLOPs (G)     | Top-1         | fp32(ms) | fp16(ms) | int8(ms) |
| ---           | ---                       | ---           | ---           | ---           | ---           | ---           | ---           |
| v2-0.75       | -                          | 2.636         | 0.20             | 69.87             | 1.04099 | 0.533396 | 0.546905 |
|     | Distilled from S3.MN-B15  | 2.636         | 0.20             | 70.18             |              |              |              |
| v2-1.0        | -                        | 3.505         | 0.30             | 72.49             | 1.18112 | 0.527927 | 0.554944 |
|     | Distilled from S3.MN-B15  | 3.505         | 0.30             | 73.30             |              |              |              |

<!-- | v2-2.0        | -                         | -             | 11.258        | 1.14             | 77.53             | -->

#### EfficientNet

| Model         | Description| Params (M)    | FLOPs (G)     | Top-1         |
| ---           | ---                        | ---           | ---           | ---           |
|EfficientNet-B3|        | 12            | 1.8           | 81.1          |
|| Distilled from S3.MN-B15  | -| - | -|
|EfficientNet-B5|        | 30            | 9.9           | 83.3          |
| | Distilled from S3.MN-B15  | -| - | -|


#### Swin Transformer

| Model         | Description| Params (M)    | FLOPs (G)     | Top-1         | fp32(ms) | fp16(ms) | int8(ms) |
| ---           | ---| ---           | ---           | ---           | ---           | ---           | ---           |
| Swin-T        |        | 29            | 4.5           | 81.3          | 6.22058   | 4.50134   | 6.13369 |
|        |  Distill from MN-B15      | 29            | 4.5           | 82.5          |   |  |  |
| Swin-S        |        | 50            | 8.7           | 83.0          | 11.2874   | 8.64826   | 11.2874 |


#### Vision Transformer

| Model         | Description   | Params (M)    | FLOPs (G)     | Top-1         | fp32(ms) | fp16(ms) | int8(ms) |
| ---           | ---    | ---           | ---           | ---           | ---           | ---           | ---           |
| ViT - B16 - 224 | Distill from MN-B15 |87.3|16.8|84.2|12.3774|3.73284|12.2015|
| ViT - L16 - 224 | Distill from MN-B15 CLS |305.3|59.6| 85.0 |39.2404|10.1443|39.4375|