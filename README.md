#**Tensorflow Projects**
A repo of everything deep and neurally related. Implementations and ideas are largely based on papers from arxiv and implementations, tutorials from the internet. 
 - ContextEncoder - Context Inpainting - a modified implementation based on the idea from [Context Encoder: Feature Learning by Inpainting](https://arxiv.org/pdf/1604.07379v1.pdf)
 - Emotion Detection - Kaggle class problem.
 - Face Detection - Face Detection as a regression problem from kaggle.
 - Generative Networks - Attempts at generative models mostly done with strided convolution and it's transposes.
 	- Image Analogy - Implementation based on Deep Visual Analogy-Making paper. Dataloader code is based on carpedm20 implementation. 
 	- Generative NeuralStyle(Johnson et al) - Needs further tuning.
 - ImageArt - Everything artistic with deep nets 
	 - DeepDream,  LayerVisualization, NeuralStyle(Gatys et al), ImageInversion(Mahendran et al) - all implementations are VGG model based.
	 - NeuralArtist(a mapping from location to rgb as an optimization problem - idea based on karpathy's convnet.js implementation)
 - MNIST - My first ever code in Tensorflow. Check this out if you are new to Deep learning and Tensorflow - based on tensorflow tutorial with additions here and there. 
 - notMNIST - Well you got to follow up MNIST with something :D
 - logs - Tensorflow Summary and Saver directory for all problems.
 - There are a couple of more implementations as attempts to solve a few other problems
	 - Deblurring - Posing blurring in images as conv net problem - architecture is based on Image super-resolution paper by Dong et al.
	 - FindInceptionSimilarity - This implementation made me realize an important concept in machine learning in general - Symbolism vs Distributed representations. 
 - TensorflowUtils - Since most of the time parameters are just given a default value.

Here are a few results,
 - Face Inpainting - Tried Context Encoder on Labeled Faces in Wild dataset and these are the results
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/ContextInpainting_logs/run1/Selection_001.png" width="298" height="480" />
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/ContextInpainting_logs/run1/Selection_002.png" width="289" height="480" />
 - Deep dreams
 
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/Deepdream_logs/checkpoints/run9/4_dp_deepdream_conv5_2.jpg" width="320" height="400" />
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/Deepdream_logs/checkpoints/run3/0_clouds_deepdream_conv5_1.jpg" width="540" height="400" />

 - Visualizing the first filter of VGG layer conv5_3
 
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/Visualization_logs/visualization_conv5_3_0.jpg" />

 - Image Inversion - An implementation based on Mahendran/Vedaldi's paper. Note that the optimization objective didn't account for variation loss across image and hence the visible noisy patterns in the result.
 
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/ImageInversion_logs/invert_check.png" width="250" height="300"/>

- NeuralArtist - Not exactly the best the network could do - but impatience got the better of me. The idea is to map a location to a RGB value and optimize a model to generate an image. If you squint a bit you will see the image better :)

<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/NeuralArtist_logs/run8/neural_artist_check.png" />

- An attempt at MNIST Autoencoder (3 bottleneck variables) - An idea borrowed from karpathy's convnet.js. As noticed in the convnet.js page running the encoder longer does reduce the error and the separation further. Here's a sample of the difference from start to 20k iterations. Different colors correspond to labels 0-9.

<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/MNIST_logs/run3/AutoEncoder_0.png" width="400" height="300"/>
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/MNIST_logs/run3/AutoEncoder_20k.png" width="400" height="300"/>

- Image Analogy - it was interesting to see how the model tries to learn. The model corresponding to just image loss seems to optimize shape followed by color and scale, though this process seems painfully slow - Rotation optimization so far doesn't seem to be visible on the horizon. Left image corresponds to result on the most trained model and the right corresponds to intermediate result. (Will be getting back to this problem later...)

<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/images/image_analogy_150k.JPG" width="300" height="450"/>

- Composite Pattern Producing Networks - Somethings are best left random and unexplained. Fun little project with the simplest of code.

<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/CPPN_logs/figure_12_64.png" width="250" height="193"/>
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/CPPN_logs/figure_16_48.png" width="250" height="193"/>
<img src="https://github.com/shekkizh/TensorflowProjects/blob/master/logs/CPPN_logs/figure_18_64.png" width="250" height="193"/>



 
