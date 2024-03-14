## Neural Network Feature Development on Image Data

### Introduction
Neural networks, mirroring the human brain’s pattern recognition abilities, have revolutionized machine learning. Their success spans various fields, from healthcare to finance,
showcasing exceptional problem-solving and data interpretation capabilities. As a neural net-
works increasingly outperform traditional algorithms, it becomes crucial to unravel their
complex learning mechanisms.
Previous studies Beaglehole et al. (2023) and Radhakrishnan et al. (2023) formulated Convolutional Neural Feature Ansatz, demonstrating that features selected by convolutional
networks can be recovered by computing the average gradient outer product (AGOP) of
the trained network with respect to image patches given by empirical covariance matrices
of filters at any given layer. Concurrently, these investigations identified an Average Gradient
Outer Product (AGOP) and Neural Feature Matrix (NFM) as key elements characterizing
feature learning in neural networks.
Meanwhile, another critical aspect of deep learning that influences neural network performance-
mance and convergence is the method of initialization. Proper Initialization is crucial; due
to the use of backpropagation in neural networks, improper initialization can lead to the
vanishing or exploding gradient problem, thereby affecting the overall training process.
Our study aims to combine the concepts of NFM and AGOP with initialization methods.
This exploration seeks to address the question: How does the application of the Neural
Feature Matrix and Average Gradient Outer Product as initialization affect the performance of neural networks?

### Feature Learning with NFM(Neural Feature Matrix) and AGOP(Average Gradient Outer Product)
* The Neural Feature Matrix (NFM), denoted by $W^TW$, is the neural feature matrix resulting from multiplying model’s weight matrices.
* The Average Gradient Outer Product (AGOP) is the average gradient outer product over patches, it is the gradient
with respect to that patch average over data.
* Previous studies posit the __Convolutional Neural Feature Ansatz__ \cite{beaglehole2023mechanism}, which states that there is a positive correlation between AGOP and NFM.
<div style="text-align:center">

$$W^TW \propto \frac{1}{n}\sum^{n}_{p=1} \nabla f(x_p)\nabla f(x_p)^T$$
</div>
*The significance of AGOP and NFM is highlighted by findings suggesting that
these measures, of early layers, perform operations similar to edge detection.
As shown in Figure 1, Patch-AGOPs and NFMs from pre-trained VGG11
identified edges in images and progressively highlighted regions of images
used for prediction

### Average Gradient Outer Product (AGOP)
The Average Gradient Outer Product (AGOP) is a concept related to the analysis of how changes in the input of a neural network affect its output, particularly in the context of understanding the network's internal representations and learning dynamics. It involves computing the outer product of the gradient of the network's output with respect to its input (or intermediate representations) and averaging this over multiple instances or over the training dataset.

### Visualizing features captured by CNFM and AGOP
We used a VGG11 model with 8 convolutional layers. We experimented on the MNIST dataset and extracted the 
values NFM and average gradient outer product (AGOP) in each layer. We looked at the correlations between the initial & trained 
CNFM and the trained CNFM & AGOP. Our investigation suggests that there is a high correlation between the trained CNFM and AGOP as 
shown in Table 1.

<img width="1104" alt="table1" src="https://github.com/hulicheng117/DSC180-website/assets/97436268/da8079c9-7f13-45a5-a288-8a0cac5589f0">

We have also plotted the first layer of CNFM and AGOP to provide visual interpretability and insight into the correlation between these two.

![figure1](https://github.com/hulicheng117/DSC180-website/assets/97436268/45a685c9-3c6b-4e7b-bbb0-ae1a644b71ff)

![figure2](https://github.com/hulicheng117/DSC180-website/assets/97436268/49ea3d39-5096-4ca1-8e0e-472ced9caa9a)

![figure3](https://github.com/hulicheng117/DSC180-website/assets/97436268/d40cb914-4735-4cd2-9956-886b46e864f2)




### Method and experiment



### Conclusion

#### Acknowledgement and References
[1] DanielBeaglehole,AdityanarayananRadhakrishnan,ParthePandit,andMikhailBelkin. Mechanism of feature learning in convolutional neural networks, 2023.\
[2] AdityanarayananRadhakrishnan,DanielBeaglehole,ParthePandit,andMikhailBelkin.Mechanism of feature learning in deep fully connected networks and kernel machines that recursively learn features, 2023.


