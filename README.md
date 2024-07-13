# Ship Detect

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

![Training Accuracy](blob:https://maixhub.com/fb572a77-2a8b-475f-8cdf-3e47b69a57e0)

## Sample Results from Validation Set

### Correct Results

![Correct Result 1](blob:https://maixhub.com/932c6b85-8f28-43da-8761-7f6d8469349c)
![Correct Result 2](blob:https://maixhub.com/7b84f460-05ad-4318-8696-2f7d69db3dc6)
![Correct Result 3](blob:https://maixhub.com/2398f8ba-fe10-47e6-9130-6b3f3c6e309f)
![Correct Result 4](blob:https://maixhub.com/59092bfb-1743-4e10-9917-483dbc20a932)
![Correct Result 5](blob:https://maixhub.com/6aa37fe2-7c30-4eed-bab2-83e5e877faf9)
![Correct Result 6](blob:https://maixhub.com/76353f48-124c-453e-8cf1-0e387b144a28)

### Incorrect Results

![Incorrect Result 1](blob:https://maixhub.com/fad05f47-edda-4eaa-bcf5-86ae9bedeaba)
![Incorrect Result 2](blob:https://maixhub.com/6f908873-99ec-4750-a3be-cd69e31f9bcc)
![Incorrect Result 3](blob:https://maixhub.com/bf33497d-3fde-4cdf-85e1-eef35bc592ad)
![Incorrect Result 4](blob:https://maixhub.com/a095267e-a6c2-4756-b3a9-99cbde06fe24)
![Incorrect Result 5](blob:https://maixhub.com/4da6c9c6-8e7b-45f9-8d03-6361d8b1a0cf)
![Incorrect Result 6](blob:https://maixhub.com/bf7f7dcc-98ca-450a-98c2-3cbf612e53e7)

> *White boxes indicate user-annotated boxes*
>
> *Green boxes indicate correctly predicted boxes by the model*
>
> *Red boxes indicate incorrectly predicted boxes by the model*
>
> *Boxes with only white outlines indicate that the model failed to detect the target*
