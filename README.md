# Comparitive Study Of Age, Ethinicity and Gender Classification via Faces
<p align="center">
  <img width="900" height="450" src="https://user-images.githubusercontent.com/54277039/171485360-c426e41d-583e-4a97-82be-1b638195caab.png">
</p>

This repository focuses on the internal working of Pre-Trained Convolutional Neural Networks (CNNs), with different architectures as follows:-

1. AlexNet :- It has 8 layers with learnable parameters. The model consists of 5 layers with a combination of Max Pooling followed by 3 fully connected layers and they use Relu activation in each of these layers, except the output layer.
2. VGG-19 :- It was proposed by Karen Simonyan and Andrew Zisserman in 2014 in the paper "Very Deep Convolutional Networks for Large Scale Image Recognition". 
3. MobileNetV2 :- An architecture with depthwise and pointwise convolutions in order to enrich the features of the input data.
4. ResNet50 :- It is a convolutional neural network that is 50 layers deep. ResNet includes several residual blocks that consist of convolutional layers, batch normalization layers and ReLU activation functions. We used the pretrained ResNet50 model to extract features from the Human Faces.

The following label columns were present alongside their corresponding variations:-

1. Age :- Discretized Integer Quantity, ranging from 1 to 100s.
2. Gender :- String based Classes, either Male or Female.
3. Ethnicity :- String based Classes; White, Black, Indian, Asian or Hispanic.

As far as the fine-tuning configurations are in concern, the following were performed:-

1. Original Image size was 48x48. It was then resized to 224x224, since most of the Neural Network Architectures follow the same input convention.
2. According to the Mean, Variance and Standard Deviation desired for the proper functionality of the pipeline, the input data was normalized (To the centralized Single-Peak Traditional Gaussian Distribution).
3. Random_Seed was set to 129, Training Epochs were set to 10 and the Train-Test Split was decided to be kept as 80-20.
4. If GPU is enabled, then Batch-Size of 64 was defined, else 32.
