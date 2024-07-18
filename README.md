# Ship Detect

## Results
-Results:
![](https://github.com/Shardul774/Ship_detect/blob/main/Img/img1.jpg)
![](https://github.com/Shardul774/Ship_detect/blob/main/Img/img2.jpg)
![](https://github.com/Shardul774/Ship_detect/blob/main/Img/img3.jpg)
![](https://github.com/Shardul774/Ship_detect/blob/main/Img/img4.jpg)
![](https://github.com/Shardul774/Ship_detect/blob/main/Img/img5.jpg)

## Requirements

**Board**
- https://wiki.sipeed.com/hardware/en/maix/maixpy_develop_kit_board/maix_duino.html

**Software**
- Kflash GUI:
   - https://github.com/sipeed/kflash_gui/releases **(Download Site)**
- MaixPy IDE:
   - https://wiki.sipeed.com/soft/maixpy/en/get_started/env_maixpyide.html **(Documentation)**
   - https://dl.sipeed.com/shareURL/MAIX/MaixPy/ide/v0.2.5 **(Download Site)**
- Micropython firmware for Maix boards:
    - https://wiki.sipeed.com/soft/maixpy/en/get_started/upgrade_maixpy_firmware.html#Download-the-firmware-to-the-development-board **(Documentation)**
    - https://dl.sipeed.com/MAIX/MaixPy/release/master/ **(Download Site)**
    - **For this project I have provided the support bin file**

**Training Model**
- https://maixhub.com/
- I have already trained a model on dataset of 3000 images as shown further in README.md, you can get the required trained model file for this project in repository.

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
