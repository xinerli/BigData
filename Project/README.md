## To Study Implementation of Gradient Descent for Multi-class Classification Using a SoftMax Regression and Neural Networks

### Yanxin Li        
Department of Statistics and Data Sciences

### Ashutosh Singh  
Operations Research and Industrial Engineering


**This is our final [project](http://rpubs.com/leexiner/bigdata-final-project) for the Fall 2017 class [SDS 385: Statistical Models for Big Data](https://github.com/jgscott/SDS385) taught by [Professor James Scott](http://jgscott.github.io/). The project has been published in RPubs with the link http://rpubs.com/leexiner/bigdata-final-project.**

**Impementation and results of the Python code can be found in the folder [Project](https://github.com/xinerli/SDS385BigData/tree/master/Project) named ````MNIST.ipynb````, ````NotMNIST.ipynb````, and ````Softmax_regression.ipynb````.**

**_For readers with time constraints, we recommend going through the Abstract, Introduction, Discussion, and Results of the report._**

##  Introduction
- We adopted a step-wise approach and started with SoftMax regression on dataset with 10 classes and then extended the work to accommodate multiple layers.

- We studied the mathematics associated with backpropagation and programmed a function that can take in a list of predictors, weights and biases and returns cross-entropy loss, modified weights and modified biases.

- The dimension and initial choices for the weights and biases depends on the design choice and must be decided by the user.

- The function is:
````Neural_network(X, y, weight, bias, step_size,  activation)````

Where,

>* X = predictors.
>* y = one hot encoded label.
>* weight = list of weights for each layer, in increasing order of layer index.
>* bias = list of bias for each layer, in increasing order of layer index.
>* step_size = step size for gradient descent.
>* activation = 0 for sigmoid, 1 for ReLU (Rectified Linear Unit).

Return,

>* Loss = cross entropy loss.
>* weight = list of modified weights for each layer, in increasing order of layer index.
>* bias = list of modified bias for each layer, in increasing order of layer index.

- The code is highly modular, and the reader can play around to create variations.
- This function can be set on a loop to fit simple Neural Networks with sufficient accuracy.
- We wrote a feed function to provide mini batches to the loop.
- The data was used after PCA transformation and dropping unimportant predictors.
- We programmed our function using **MNIST** data set and we cross checked the function by fitting various Neural Networks configurations on different models.
- We have presented the work for one such dataset, called **notMNIST**. The dataset is like MNIST with 10 classes of English alphabets from A to J.

## Dataset

The dataset can be downloaded from the following link: 

- **MNIST**: http://yann.lecun.com/exdb/mnist/

- **notMNIST**: http://yaroslavvb.com/upload/notMNIST/

## Shout-outs
A big thank you to Professor James Scott who helped us with the optimization of the Neural Networks and taught a great class this semester.
