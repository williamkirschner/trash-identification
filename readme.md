# Trash Identification
A deep learning model capable of identifying various solid waste items such as glass, paper, cardboard, plastic, metal, and trash.

## Requirements
* [Pytorch 1.13+](https://pytorch.org/get-started/locally/)
* [Numpy 1.16.4+](https://pypi.org/project/numpy/)
* [Matplotlib 3.1.1+](https://pypi.org/project/matplotlib/)

## Dataset
[Trashnet](https://github.com/garythung/trashnet): 2527 Images - 2274 Training (90%) & 253 Validation (10%)
* 501 Glass
* 594 Paper
* 403 Cardboard
* 482 Plastic
* 137 Trash
* 410 Metal

## Process
1. Reorganize Dataset to have a training and validation directories with subdirectories containing each category
2. Initalize the pretrained model
3. Reshape the final layer(s) to have the same number of outputs as the number of classes in the new dataset (6)
4. Define for the optimization algorithm which parameters we want to update during training
5. Run the training step

## Model
| Model Name | Accuracy | Time*     |
|------------|----------|----------|
| Resnet     | 0.953125 | 26m 50s  |
| Alexnet    | 0.914062 | 13m 23s  |
| VGG        | 0.960938 | 59m 23s  |
| Squeezenet | 0.941406 | 15m 10s  |
| Densenet   | 0.964844 | 29m 34s  |
| __Inception__  | __0.972656__ |  40m 56s |

![graph](https://imgur.com/M4oRGEN.png)
_*Can be reduced using more powerful GPUs, reducing its importance for now._

## To Do
- [x] Try with various architectures
- [ ] Save and export model for post-training evaluation to finetune hyperperameters

## Acknowledgements
Thank you [@garythung](https://github.com/garythung) for the dataset and [@mpcrlab](https://github.com/mpcrlab) for the help
