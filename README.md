# liar_yolov5x
#Layer-interaction attention reinforced YOLOv5x with object-mosaic in the power line asset detection 

## Introduction
There are different line assets such as transmission tower,damper,insulators,spacers,and tower plates 
on the high voltage transmission line. The detection and classification of these assets in transmission 
lines is essential for the safety and stability of power systems... For more details, please refer to our [paper]().

## Installation
Use `git clone https://github.com/ultralytics/yolov5/tree/v5.0`
to clone the project,the code modification is based on yolov5x,
the [dataset](https://pan.baidu.com/s/1Cb2DQuI2l-ilpC7Y1n5ztw?pwd=1234) concluded train set and test set 
and the [pre-training weight](https://pan.baidu.com/s/1CHCU8Saa_cHRc6SjfBZ8aw?pwd=1234)is in the direction `weight`.
For training of other models, please refer to [mmdetection](https://github.com/open-mmlab/mmdetection).
We have uploaded all the information related to the project to the folder.

## Training
You can use the following commands for training:

    python train.py --device 'your device' 
                    --datapath 'your path of dataset' 
                    --num-classes 'number of detected categories (excluding background)'
                    --output_dir 'path where to save log' 
                    --resume 'pre-training weights' 
                    --start-epoch 'start epoch'
                    --epoch 'number of total epochs to run' 
                    --batch_size 'batch size when training'
    
such as:

    python train.py --device 'cuda:0' \
                    --datapath './data' \
                    --num-classes 2 \
                    --output_dir './save_weights' \
                    --resume './pre_training_weights/your_weights.pth' \
                    --epoch 300 \
                    --batch_size 16

