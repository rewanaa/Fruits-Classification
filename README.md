# Report on Architectural Performance
This is an analysis of model performance in a chronological order, emphasizing the historical evolution of architectural approaches using a collection of different datasets. Introducing state-of-the-art models to underscore distinctions and conduct a thorough comparison. 

We experimented with various hyperparameter settings, and we evaluate the models based on a variety of criteria, encompassing training and validation accuracy, loss function, model size, and inference time.

Additionally, we implemented two ensemble techniques to enhance accuracy, yielding higher accuracy results. 

## Data Preprocessing
1. Normalization.
2. Random Augmentation (flipping, rotation, changing colors, etc.).
3. Resize.
4. Random Erasing (for more generalization).

## Hyperparameters Used
- Tested batch sizes: 64, 128, 256.
- Experiments extended beyond 25 epochs.
- Utilized optimizers: SGD, Adam, and AdamW.
- Varied learning rates for AdamW: 0.01, 0.003, 0.001.
- Applied the CosineAnnealingLR scheduler to optimize the training process.
- Used (Adaptive) SAM Optimizer

## Model Evaluation: Validation and Train Accuracy, and Loss Comparison
We conducted multiple experements using different hyperparameters, and used a pre-trained ConvNext model as the benchmark for the state of the art accuracy, which result to GoogleNet and MobileNet acheving the highest accuracy
![image](https://github.com/rewanaa/Fruits-Classification/assets/73082049/7d3f4c7a-ef4b-4f12-b4d5-726a9fbced22)
![image](https://github.com/rewanaa/Fruits-Classification/assets/73082049/f49f1dd0-b400-4c37-a812-863441e94116)


## Model Evaluation: Size, Accuracy, and Inference Comparison
We use the Maximum reached validation accuracy to compare between the models, we compared the accuracy gained from increasing it shows that with more complex models have higher accuracy, this is shown in ConvNext as it has the highest accuracy that dominate the comparison.
We also conducted that simple model could exceed more complex one, this is because of the architecture properties can help the model reach better Accuracy, thus we conclude that simpler models with better architecture like ResNet can exceed more complex old model like AlexNet
![image](https://github.com/rewanaa/Fruits-Classification/assets/73082049/04a61ea9-3c7a-4e62-8740-bae9b18119d2)


## Models Scores
| Model             | Train Accuracy | Validation Accuracy |
|-------------------|----------------|----------------------|
| AlexNet           | 70.38%         | 66.26%               |
| VGG               | 37.55%         | 46.26%               |
| ResNet            | 63.22%         | 65.86%               |
| MobileNet         | 76.07%         | 73.54%               |
| GoogleNet         | 88.13%         | 82.02%               |
| DenseNet          | 68.31%         | 70.91%               |
| ConvNext          | 98.69%         | 95.51%               |
| Ensemble          | 98.67%         | 98.55%               |
| Transformer (VIT) | 77.61%         | 73.33%               |

## Dataset
link
