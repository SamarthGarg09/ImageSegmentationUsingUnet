# ImageSegmentationUsingUnet
### Datasets info
Used [Oxford Pets - IIT dataset](https://www.robots.ox.ac.uk/~vgg/data/pets/).This contains pet images, their classes, segmentation masks and head region-of-interest. (Also available in tensorflow datasets.)
segmentation masks or label map has 3 classes that are `{'pet', 'background', 'outline'}`
| Label            | Class Name     |
| -------------    | -------------  |
| 0                | PetImage       |
| 1                | Background     |
| 2                | Outline        |
### Model - Unet
Its architecture consists of `{`encoder`, `baseline`, `decoder`}` blocks respectively.

<img src='https://drive.google.com/uc?export=view&id=1BeQSKL2Eq6Fw9iRXsN1hgunY-CS2nH7V' alt='unet'>

#### A UNet consists of an encoder (downsampler) and decoder (upsampler) with a bottleneck in between. The gray arrows correspond to the skip connections that concatenate encoder block outputs to each stage of the decoder.
Model is trained for 10 epochs but for better accuracy, one can train model for more epochs.

Used IOU and Dice scores for metrics evaluation.
