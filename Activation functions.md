Non-linearities or non-linear activation functions are an important addition to NN architectures in that they solve the issue that the sum of linear functions yields a linear function. Through this non-linearity the depth of deep learning architectures can be properly utilised to tackle complex problems.

The sigmoidal logistic function: $\sigma(z) = \frac{1}{1 + e^{-z}}$ is commonly referred to as the [[sigmoid function]] in ML literature. The use of this function as a non-linearity is problematic in that highly negative inputs will result in an output that is close to zero and as a result the NN will learn quite slowly and will be more likely to be trapped within local minima in the loss landscape throughout the training process. 

These considerations result in hyperbolic tangent ([[tanh]]) being used more often. 
