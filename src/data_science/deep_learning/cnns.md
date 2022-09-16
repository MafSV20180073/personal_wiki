# Convolutional Neural Networks

***
<u>A simple definition of a CNN</u>: a type of neural network which builds progressively higher-level features out of groups of pixels commonly found in the images.
***

<br>

### Progressive resizing

- A technique for building CNNs where models are initially trained using small-images (small images tend to generalize well to larger input sizes and take less time to train). The scaling up of the images and the models is done later;
- We start by building a classifier that performs well on tiny n x n images, and the next step can be scaling those models up to 2n x 2n images;
- The previous step is performed through transfer learning;
- Article with use-case of progressive resizing: https://towardsdatascience.com/boost-your-cnn-image-classifier-performance-with-progressive-resizing-in-keras-a7d96da06e20
