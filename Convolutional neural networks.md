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



