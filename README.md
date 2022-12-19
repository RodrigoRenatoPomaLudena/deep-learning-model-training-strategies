# deep-learning-model-training-strategies
In this project, it's evaluated multiple strategies for deep learning model trainning using the MNIST dataset of KERAS.
This document it's divided in four sections:
1. Variate the characteristics of deep learning models to choose the best by accuracy score and sparse categorical crossentropy loss. 
2. Validate in which case is necessary the use of BATCH NORMALIZATION as explained in *Batch Normalization: Accelerating Deep Network Training by Reducing Internal Covariate Shift* (DOI: https://doi.org/10.48550/arXiv.1502.03167)
3. Using different OPTIMIZERS available in KERAS libraries, validate which one is the best for the selected model. Comparing our results with the ones in *Adam: A Method for Stochastic Optimization* (DOI: https://doi.org/10.48550/arXiv.1412.6980) 
4. We add two hidden neural network: Conv2D and MaxPooling2D. With these additions we expected to increase the value of accuracy as referred in *t-SNE for Feature Visualization* (https://learnopencv.com/t-sne-for-feature-visualization/)

# Standard characteristics in models
- Metrics: accuracy
- Loss: sparse_categorical_crossentropy
- Validation set: first 5000 values
- Trainning set: first 55000 values after 5001 index
- Test set: 10000 default values
- Optimizer: SGD

# Section 1
The main variations that are made in the models are: 
- architecture
- activation functions
- kernel initializers
- learning rates
- optimizers.

# Section 2
The activation functions are replaced by sigmoids with batch normalization type layers in the best model of SECTION 1. Also, the learning rate is changed to 5 times its original value. Then we compare both models (Section 1 vs Section 2) to validate if the changed proposed in the papper improves the accuracy and reduce the loss.

# Section 3
The standard optimizer is changed, using the default values of the their parameters, with these optimizers:
- SGD
- Momentum
- Nesterov
- AdaGrad
- RMSProp
- ADAM

# Section 4
The best model in SECTION 1 changed by adding two layers of neural networks: Conv2D and MaxPooling2D. We expect those layers after the input layer to significantly improve accuracy.

# Contributors
[@NantoCaparachin](https://github.com/NantoCaparachin)
