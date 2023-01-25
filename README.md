# Convolution Neural Network

## Why use CNN instead of Deep Neural Network for Image recognition? 

**Parameter Explosion**: In Fully Connected Deep Neural Network, each and every node of one layer is connected to each and every node of its preceding or following layer. This connection happens through the use of weights and possibly bias too. Therefore, for a large image - say 100 x 100 pixel - the zeroth layer (input layer) will have 10K nodes. The interconnection between this layer will be of the order O(10K x 10K = 100M). Thus, Dense Fully Connected NNs require massive computational power. Using CNN results in requiring dramatically fewer parameters - creating sparse NNs- to train and attain similar or better performance. 

**Location Invariance**: When we feed an image in 2D to the Fully Connected Layer, it has to be flattened into a column matrix. That means such layers do not provide feature extraction with location invariance. A puppy at the top left corner in one image might not be identified when it is in the bottom right of another image. CNN addresses this spatial weakness of the Deep NN. 

**Visual Stimulus of Eye**: CNNs are modeled on how our eye perceives an image. Our eye perceives visual stimulus in a 2D visual field called Local Receptive Field. Eye then sends this 2D image to the visual cortex that lies in our brain and is responsible for interpreting the image. It also adds depth perception. CNN is designed to interpret the image and add depth perception using the layers of the CNN. Individual layers of CNN focus on a small field at a time. DNNs are not good at extracting such features despite their much larger computational requirement. 


## Image Pre-processing methods: 
1. Uniform Aspect Ratio - many frameworks prefer to work with square shaped images, or at least images with uniform aspect ratio. Since most of the images contain the most information towards the center of the image, center-cropping is meaningful. 
2. Uniform Image Size - All images in a single batch need to be of the same size (height x width). Rescaling the image to fit to the feature map we plan to use later on. - upscaling or down-scaling
3. Mean & Perturbed Images - mean image is the average pixel value across the entire training dataset. Important features can emerge, and common patterns can be detected. Example, faces in the center of the image. 
4. Perturbed image: Intentionally distort pixels by varying them from the mean image. Makes CNN robust by preventing it from focusing only in the center of the images. 
Normalized Image Inputs - NNs will train faster if the images are normalized around the mean. 
5. Dimensionality Reduction - if images are very large. Color RGB images with 3 channels can be reduced to single channel grayscale. This helps reduce the size of the problem so that training completes faster. Also, it might help extract latent but significant features from the underlying data so  that the neural network does not need to deal with irrelevant features. 
6. Augmentation - Perturbed images are examples of data augmentation. Scaling, rotation, affine transformation. Makes CNN more robust and prevents overfitting. 

