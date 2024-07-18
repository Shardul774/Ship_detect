# Ship Detect
## Board 
https://wiki.sipeed.com/hardware/en/maix/maixpy_develop_kit_board/maix_duino.html

## Dataset

The dataset consists of 2 labels and 3000 images. The composition is as follows:

| Label         | Training / Validation | Total |
| ------------- | --------------------- | ----- |
| Authorized    | 1491 / 166            | 1657  |
| UnAuthorized  | 1231 / 137            | 1368  |

## Training Parameters

**Image Augmentation**
- Random Mirror: Off
- Random Rotation: Off
- Random Blur: On
- Scaling Method: Contain
- Scaling Size: 224 x 224
- Mean: 123.5
- Standard Deviation: 58.395

**Model Information**
- Deployment Platform: nncase
- Model Network: yolov2
- Backbone Network: mobilenet_0.75

**Training Parameters**
- Number of Epochs: 100
- Batch Size: 50
- Learning Rate: 0.001
- Bounding Box Limit: 10
- Data Balancing: On
- Allow Negative Samples: On

## Training Results

The best accuracy on the validation set was achieved at the 90th training iteration: 0.785.

![Training Accuracy](https://github.com/Shardul774/Ship_detect/blob/main/Img/loss_acc.png)

## Sample Results from Validation Set

### Correct Results

![Correct Result 1](https://github.com/Shardul774/Ship_detect/blob/main/Img/download.jpeg)
![Correct Result 2](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%205.jpeg)
![Correct Result 3](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%206.jpeg)
![Correct Result 4](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%204.jpeg)
![Correct Result 5](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%203.jpeg)
![Correct Result 6](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%202.jpeg)

### Incorrect Results

![Incorrect Result 1](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%20(1).jpeg)
![Incorrect Result 2](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%20(2).jpeg)
![Incorrect Result 3](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%20(3).jpeg)
![Incorrect Result 4](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%20(4).jpeg)
![Incorrect Result 5](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%20(5).jpeg)
![Incorrect Result 6](https://github.com/Shardul774/Ship_detect/blob/main/Img/download%20(6).jpeg)

> *White boxes indicate user-annotated boxes*
>
> *Green boxes indicate correctly predicted boxes by the model*
>
> *Red boxes indicate incorrectly predicted boxes by the model*
>
> *Boxes with only white outlines indicate that the model failed to detect the target*
