# Deep Learning Using Keras,Tensorflow
## material of pythonprogramming.net


Welcome we'll be discussing Convolutional Neural Networks (Convnets and CNNs), using one to classify dogs and cats with the dataset we built in 1 notebook.

The Convolutional Neural Network gained popularity through its use with image data, and is currently the state of the art for detecting what an image is, or what is contained in the image.

The basic CNN structure is as follows: Convolution -> Pooling -> Convolution -> Pooling -> Fully Connected Layer -> Output

Convolution is the act of taking the original data, and creating feature maps from it.Pooling is down-sampling, most often in the form of "max-pooling," where we select a region, and then take the maximum value in that region, and that becomes the new value for the entire region. Fully Connected Layers are typical neural networks, where all nodes are "fully connected." The convolutional layers are not fully connected like a traditional neural network.

Okay, so now let's depict what's happening. We'll start with an image of a cat:

![cat](https://pythonprogramming.net/static/images/machine-learning/cat-example.png)

Then convert this image to pixels:

![pixel](https://pythonprogramming.net/static/images/machine-learning/pixelated-image-example.png)

For the purposes what we want to do, assume each square is a pixel. Next, for the convolution step, we're going to take a certain window, and find features within that window:

![window](https://pythonprogramming.net/static/images/machine-learning/convolution-window.png)

That window's features are now just a single pixel-sized feature in a new featuremap, but we will have multiple layers of featuremaps in reality.

Next, we slide that window over and continue the process. There will be some overlap, you can determine how much you want, you just do not want to be skipping any pixels, of course.

![sliding](https://pythonprogramming.net/static/images/machine-learning/convolution-stride.png)

Now you continue this process until you've covered the entire image, and then you will have a featuremap. Typically the featuremap is just more pixel values, just a very simplified one:

![featuremap](https://pythonprogramming.net/static/images/machine-learning/convolution-new-featuremap.png)

From here, we do pooling. Let's say our convolution gave us (I forgot to put a number in the 2nd row's most right square, assume it's a 3 or less):

![pooling](https://pythonprogramming.net/static/images/machine-learning/convolution-example.png)

Now we'll take a 3x3 pooling window:

![3*3](https://pythonprogramming.net/static/images/machine-learning/pooling-window.png) 

The most common form of pooling is "max pooling," where we simple take the maximum value in the window, and that becomes the new value for that region.

![maxpool](https://pythonprogramming.net/static/images/machine-learning/max-pool.png)

We continue this process, until we've pooled, and have something like:

![final](https://pythonprogramming.net/static/images/machine-learning/max-pooling-example.png)

Each convolution and pooling step is a hidden layer. After this, we have a fully connected layer, followed by the output layer. The fully connected layer is your typical neural network (multilayer perceptron) type of layer, and same with the output layer.

## material used of  pythonprogramming.net
