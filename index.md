## Neural Network Feature Development on Image Data

#### Introduction
Neural networks, mirroring the human brain’s pattern recognition abilities, 
have revolutionized machine learning. Their success spans various fields, 
from healthcare to finance, showcasing exceptional problem-solving and data interpretation capabilities. 
As neural networks increasingly outperform traditional algorithms, it becomes crucial to unravel their complex learning mechanisms. 
This understanding not only advances our knowledge but also opens doors to more robust and efficient applications. 
Our project aims to delve into these intricacies, offering deeper insights into the functioning of neural networks and their 
evolving role in modern technology.

The study of feature evolution throughout the training phase in neural networks is pivotal in advancing our 
understanding of modern machine learning methodologies. The previous studies Beaglehole et al. (2023) and Radhakrishnan et al. (2023) formulated Convolutional
Neural Feature Ansatz, in which the features selected by convolutional networks can be recovered by computing the average gradient outer product (AGOP) of the trained network with 
respect to image patches given by empirical covariance matrices of filters at any given layer. 

In this work, we are going to concentrate on examining the progression of image data
features within convolutional networks, specifically through the lens of training VGG11 models on the CIFAR-10 dataset. Our investigation delves into the selection process 
of features by individual filters and their increasing significance in capturing the intrinsic patterns present in the data. By elucidating the path of feature evolution in neural networks, 
our aim is to shed light on their learning dynamics, potentially paving the way for enhanced performance in tackling more sophisticated tasks.

#### Neural Feature Matrix (NFM) 
The Neural Feature Matrix (NFM) refers to the representation of features in a neural network. In deep learning, features are the individual measurable properties or characteristics of the phenomenon being observed. The NFM essentially represents how these features are encoded or transformed by a neural network. This matrix can be thought of as a structured way to represent the information that the network has learned about the data. 

#### Average Gradient Outer Product (AGOP)
The Average Gradient Outer Product (AGOP) is a concept related to the analysis of how changes in the input of a neural network affect its output, particularly in the context of understanding the network's internal representations and learning dynamics. It involves computing the outer product of the gradient of the network's output with respect to its input (or intermediate representations) and averaging this over multiple instances or over the training dataset.

#### Visualizing features captured by CNFM and AGOP
We used a VGG11 model with 8 convolutional layers. We experimented on the MNIST dataset and extracted the 
values NFM and average gradient outer product (AGOP) in each layer. We looked at the correlations between the initial & trained 
CNFM and the trained CNFM & AGOP. Our investigation suggests that there is a high correlation between the trained CNFM and AGOP as 
shown in Table 1.

<img width="1104" alt="table1" src="https://github.com/hulicheng117/DSC180-website/assets/97436268/da8079c9-7f13-45a5-a288-8a0cac5589f0">

We have also plotted the first layer of CNFM and AGOP to provide visual interpretability and insight into the correlation between these two.

![figure1](https://github.com/hulicheng117/DSC180-website/assets/97436268/45a685c9-3c6b-4e7b-bbb0-ae1a644b71ff)

![figure2](https://github.com/hulicheng117/DSC180-website/assets/97436268/49ea3d39-5096-4ca1-8e0e-472ced9caa9a)

![figure3](https://github.com/hulicheng117/DSC180-website/assets/97436268/d40cb914-4735-4cd2-9956-886b46e864f2)




#### Method and experiment



#### Conclusion

![figure2](https://github.com/hulicheng117/DSC180-website/assets/97436268/49ea3d39-5096-4ca1-8e0e-472ced9caa9a)

![figure3](https://github.com/hulicheng117/DSC180-website/assets/97436268/d40cb914-4735-4cd2-9956-886b46e864f2)

#### Acknowledgement and References
[1] DanielBeaglehole,AdityanarayananRadhakrishnan,ParthePandit,andMikhailBelkin. Mechanism of feature learning in convolutional neural networks, 2023.\
[2] AdityanarayananRadhakrishnan,DanielBeaglehole,ParthePandit,andMikhailBelkin.Mechanism of feature learning in deep fully connected networks and kernel machines that recursively learn features, 2023.


