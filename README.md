# reCAPTCHASolver
In this model, I use transfer learning with the VGG16 model to label reCAPTCHA images. The training dataset is from https://github.com/deathlyface/recaptcha-dataset.

VGG16 is a convolutional neural network model proposed at the University of Oxford in the paper “Very Deep Convolutional Networks for Large-Scale Image Recognition”. The model achieves 92.7% top-5 test accuracy in ImageNet, which is a dataset of over 14 million images belonging to 1000 classes.

Using the pre-trained network on images not in the training set is called transfer learning. Here, I use transfer learning to train a network to classify reCAPTCHA images with an overall accuracy of 82%.

Note: I edited out some of the data because it had classes that the VGG16 model was not trained to recognize and therefore would be less effective with. Then, I removed a bit more of the data so that there would be a balanced distribution of around 1000 images per class. This is important so that the model does not guess car every time and get it right half the time because there would be 3000 images of a car.

Here's a link to an article I wrote on this: https://ryansh3n.medium.com/cracking-recaptchas-with-cnns-and-transfer-learning-edc26ab675ec - this contains more high-level knowledge about what CNNs and transfer learning is.

Here's a link to the video I made where I go more in-depth in the code and explain my though process: https://youtu.be/eSK3fKKZroI
