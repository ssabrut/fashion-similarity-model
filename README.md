# Fashion Similarity Model
This project aims to build a fashion similarity model using TensorFlow MNIST Datasets and Siamese Network with custom model and contrastive loss. The model can compare two images of clothing items and determine how similar they are.

## Dataset
The dataset used for this project is the [Fashion MNIST](https://www.tensorflow.org/datasets/catalog/mnist) dataset, which contains 70,000 grayscale images of 10 different types of clothing items, such as t-shirts, trousers, dresses, etc. Each image has a size of 28x28 pixels and a label from 0 to 9.

## Model
The model used for this project is a Siamese Network, which consists of two identical sub-networks that share the same weights and parameters. The sub-networks are custom models that have four convolutional layers and two dense layers. The output of the sub-networks is a 128-dimensional feature vector that represents the image. The base network architecture will looked like this.

<img src="https://github-production-user-asset-6210df.s3.amazonaws.com/53653797/244704422-3099b3ca-f709-4ba8-a512-0fc5f28846f8.png" style="transform: rotate(90deg);">

The model takes two images as input and passes them through the sub-networks. Then, it computes the Euclidean distance between the feature vectors and applies a sigmoid function to get a similarity score between 0 and 1. The closer the score is to 1, the more similar the images are.

![](https://github.com/ssabrut/fashion-similarity-model/blob/main/siamese-model.png)

The model is trained using contrastive loss, which is a function that measures how well the model can distinguish similar and dissimilar pairs of images. The loss function encourages the model to minimize the distance between similar pairs and maximize the distance between dissimilar pairs.

## Usage
To use this project, you need to have Python 3.6 or higher and TensorFlow 2.0 or higher installed on your machine.

## Results
The model achieved an accuracy of 90% on the test set, which means that it correctly classified 90% of the pairs of images as similar or dissimilar. The less distance are more similar with each other
Here are some examples of the model’s predictions:

![image](https://github.com/ssabrut/fashion-similarity-model/assets/53653797/f3bf3b1c-2856-4c9f-8595-5466e1c8dc01)
![image](https://github.com/ssabrut/fashion-similarity-model/assets/53653797/36496dfa-fe8b-457f-b3ea-443333d0a84e)
