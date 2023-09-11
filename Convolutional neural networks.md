- CNNs are a family of models that were originally inspired by the manner in which the visual cortex of the human brain functions when recognising objects.
- The development of these models originates in the 90s when LeCun and colleagues proposed this novel NN architecture for the task of classifying handwritten digits from images.

## CNNs and feature hierarchies 

Extracting key salient features from data is key to creating performant ML algorithms. Traditional ML models rely on input features derived from domain experts or some computational feature extraction mechanism. 

CNNs are an example of a neural net architecture that have the ability to learn these salient features from raw data. The key concept here is that these models learn key features that are relevant for a particular task. As this structure is used in layers there also exists the ability to construct a hierarchy in that earlier layers will focus on the extraction of low level features and the deeper layers can these use these fundamental features to predict some target value or class label. 

Deep CNNs have the ability to construct a feature hierarchy in that these fundamental features captured by the earlier layers can be combined to form more complex higher level features.

CNNs compute feature maps from a given input image, in which each element is derived from a local patch of pixels found within the input image. These local patches of pixels are termed the local receptive field. 

The performance of CNNs in relation to image data can be attributed to two key considerations:

- **Sparse connectivity**. A single element within our feature map is only connected to a small region of pixels. This is contrasted to how MLPs function using image data in which a layer is connected to every pixel in the image.
- **Parameter sharing**. The same parameter weights can be used for different receptive fields of a given input image.

From these two considerations, replacing regular fully connected MLP layers with a convolution layer allows for a significant decrease in the number of parameters a model requires concurrently with an increase in the models ability to capture key salient features. This follows with our intuitive prior on image data in that pixels close together should be more relevant to one another relative to those more distant to one another.

Typical CNN architecture will consist of several convolutional and sub-sampling layers that are followed by fully connected layers toward the tail end of the model. Subsampling layers or [[Pooling layers]] do not contain any learnable parameters (no weights or bias in this layer). 

## Discrete convolutions

A discrete convolution is the fundamental operation within a CNN.

A discrete convolution for two vectors $x$ and $w$ is denoted by $y = x * w$. Note that $*$ indicates the convolution operation and not multiplication.  

![[Pasted image 20230910104608.png]]


## [[Subsampling layers]]

Subsampling is often applied in one of two forms of pooling operations within the context of CNNs:

- Max pooling
- Mean-pooling (average pooling)

The size of the region where the pooling operation is performed is referred to as the pooling size.

### Advantages of pooling

- Pooling (max-pooling) introduces a mechanism of local in-variance in that small changes in the local region will not influence the result of max-pooling. This is important for generating features that are robust to noise found within the input data.


