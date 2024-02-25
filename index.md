## Data Science Capstone Project: [Project Title]

Neural networks, mirroring the human brain’s pattern recognition abilities, 
have revolutionized machine learning. Their success spans various fields, 
from healthcare to finance, showcasing exceptional problem-solving and data interpretation capabilities. 
As neural networks increasingly outperform traditional algorithms, it becomes crucial to unravel their complex learning mechanisms. 
This understanding not only advances our knowledge but also opens doors to more robust and efficient applications. 
Our project aims to delve into these intricacies, offering deeper insights into the functioning of neural networks and their 
evolving role in modern technology.

The study of feature evolution throughout the training phase in neural networks is pivotal in advancing our 
understanding of modern machine learning methodologies. The previous studys Beaglehole et al. (2023) and Radhakrishnan et al. (2023) formulated Convolutional
Neural Feature Ansatz which the features selected by convolutional networks can be recovered by computing the average gradient outer product (AGOP) of the trained network with 
respect to image patches given by empirical covariance matrices of filters at any given layer. 

In this paper, we are going to concentrates on examining the progression of image data
features within convolutional networks, specifically through the lens of training ResNet-18 and LeNet models on the MNIST dataset. Our investigation delves into the selection process 
of features by individual filters and their increasing significance in capturing the intrinsic patterns present in the data. By elucidating the path of feature evolution in neural networks, 
our aim is to shed light on their learning dynamics, potentially paving the way for enhanced performance in tackling more sophisticated tasks.

#### Method and experiment
In this project, we are going to use the MNIST (Modified National Institute of Standards and Technology database). The MNIST dataset is a large database consisting of handwritten digits ranging from 0 to 9, where each image is a 28x28 pixels in size.
Moving forward, possible datasets to investigate includes ImageNet and CIFAR-10...

We used a VGG11 model with 8 convolutional layers. We experimented on the MNIST dataset and extracted the 
values W T W and average gradient outer product (AGOP) in each layer. We looked at the correlations between the initial & trained 
CNFM and the trained CNFM & AGOP. Our investigation suggests that there is a high correlation between the trained CNFM and AGOP as 
shown on Table 1.


<img width="1104" alt="table1" src="https://github.com/hulicheng117/DSC180-website/assets/97436268/da8079c9-7f13-45a5-a288-8a0cac5589f0">

We have also plotted the first layer of CNFM and AGOP to provide visual interpretability and insight into the correlation between these two.

![figure1](https://github.com/hulicheng117/DSC180-website/assets/97436268/45a685c9-3c6b-4e7b-bbb0-ae1a644b71ff)


#### Result

![figure2](https://github.com/hulicheng117/DSC180-website/assets/97436268/49ea3d39-5096-4ca1-8e0e-472ced9caa9a)

![figure3](https://github.com/hulicheng117/DSC180-website/assets/97436268/d40cb914-4735-4cd2-9956-886b46e864f2)



