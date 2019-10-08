# GAN-dog-generator
In this exercise I followed along with this article: https://towardsdatascience.com/dcgans-generating-dog-images-with-tensorflow-and-keras-fb51a1071432

And attempted to generate images that look like dogs using the following dataset: http://vision.stanford.edu/aditya86/ImageNetDogs/

My only issue was that the dataset the article uses is structured a bit differently since that one was from Kaggle and since that isn't available for download anymore I had to use the source. This required a couple of extra steps.

I'm using a simplfied code than what the article goes through in some respect such as:
  - No spectral normalization.
  - No relativistic loss function
  - No evaluation
  
 I also added some changes to the coda from the article:
  - When I crop the images I took out some seemingly unnecessary calculations and I also save these cropped images. I do this because cropping out the new images can take quite a while and simply loading them up from a new folder is faster. One was to improve this even more would be to use a generator.
Added reloading of the model weight before training so after kernel restart I continue from where I left off. Now that I understand the code better I would like to try out the features I left out (spectral normalization, evaluation) and also try out new datasets. I'd also like to spend some time later tuning the Hyperparameters more.

Below you can see some of the pictures the model generated after some training:

![alt text](https://github.com/mgabor922/GAN-dog-generator/blob/master/Image_at_epoch_0040.png)
