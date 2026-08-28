CIFAR-10 Image Classification with CNNs

/Overview
This project explores image classification on the CIFAR-10 dataset with three models:
- Baseline Multilayer Perceptron (MLP)
- CNN without data enhancement 
- CNN with data enhancement
The goal is to analyze the performance of CNNs against a fully connected baseline and to determine the impact of data augmentation on generalization.

/Dataset
CIFAR-10 consists of 60,000 RGB images (32×32 pixels), categorized into 10 classes:
airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck.
The dataset was divided into training, validation, and test sets.

/Models
- MLP Benchmark Model
An image pixel-based fully connected network that operates on a flattened format.
-CNN
A convolutional neural network featuring convolution, batch normalization, ReLU activation, max pooling, and dropout.
-CNN with Data Augmentation
The same CNN architecture was trained using random crops and horizontal flips.

/Results
| Model | Validation Accuracy | Test Accuracy |
|---|---:|---:|
| MLP | 52.46% | 52.46% |
| CNN – No Augmentation | 81.78% | 81.78% |
| CNN – With Augmentation | 79.22% | 79.22% |

The CNN without augmentation achieved the highest measured accuracy in this experiment.
Although data augmentation decreased the train/validation generalization gap and demonstrated improved resistance to overfitting, it sadly did not improve the final validation or test accuracy in this run.

/How to Run
Install the required packages:
```bash
pip install -r requirements.txt
