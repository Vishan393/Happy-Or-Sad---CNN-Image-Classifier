<h1>CNN Image Classification Project - Happy or Sad People</h1>

<p>This project is an image classification project using Convolutional Neural Networks. The goal of the project is to identify whether a person is happy or sad. The project uses <strong>Tensorflow-GPU</strong> along side <strong>OpenCV</strong> and <strong>Matplotlib</strong> inside of a <strong>Conda environment</strong>. The whole project is written in Jupyter Notebooks.</p>

> This Image Classification project can be used for almost any image.

<p>&nbsp;</p>

<h1>Background</h1>
<p>Convolutional Neural Networks: Neural Networks specifically used for image recognition.</p>
<ul>
    <li>Tensorflow: Is used to create various machine learning models</li>
    <li>OpenCV: Is an open computer vision module </li>
    <li>MatplotLib: Is used for visualization</li>
</ul>

<p>&nbsp;</p>

<h1>Setup</h1>

<p>The first step is to install all the dependencies into an Anaconda Environment. We use Anaconda because it makes working with virtual environments easier, especially with Tensorflow.</p>

<p>Then we limit the GPU memory usage of TensorFlow. If the amount of GPUs available is blank, Tensorflow is not installed correctly and why I decided to use a Conda environment.</p>

<p>&nbsp;</p>

<h1>Data Cleaning</h1>
<p>Once the setup is complete, we then import the data and clean it.</p>
<p>The data is downloaded from Google using the "Download All Images" extension. This will download all the images which we will clean through afterwords.</p>
<p>Once we have all the images in the data folder. We clean the images with OpenCV. We do this by creating a script that removes any image that does not have the desired extension. We also manually delete any images under 10 KB since these images are too small for our model.</p>

<p>&nbsp;</p>

<h1>Creating Data Pipeline</h1>
<p>We load the data into a dataset using keras, creating the pipeline.</p>
<p>We determine the labels for the images by displaying a segment of a batch and crossreferencing the value.</p>

<p>&nbsp;</p>

<h1>Split Data</h1>
<p>We Scale all the image between 0 to 1.</p>
<p>Then we split the dataset into batches and assign 70% to testing data, 20% to validation data, and 10% to testing data.</p>

<p>&nbsp;</p>

<h1>Building the Model</h1>
<p>We create the CNN Model by using TensorFlow Keras Sequential models.</p>
<p>The neural network has 9 layers, 3 Conv2D layers, 3 MaxPooling2D layers, 1 Flattern layer, and 2 Dense layers. The neural network uses Relu and Sigmoid activation functions.</p>

<p>&nbsp;</p>

<h1>Training and Testing the Model</h1>
<p>We train the model with the testing and validation data batches for 20 iterations.</p>
<p>We then plot the accuracy values and the loss values in a graph using Matplotlib for visualization. If the loss function is not decreasing while the accuracy function is increasing, this may be because of a few options:</p>
<ul>
    <li>The data is inadequate</li>
    <li>The data is not accurate</li>
    <li>The selected model is faulty</li>
</ul>
<p>Finally, we test the model with the remaining testing batches and verify our results.</p>

<p>&nbsp;</p>

<h1>Saving the Model</h1>
<p>The last step in the project is to save the model into the models folder so we can use this for future applications.</p>
<p>In the runModel Jupyter Notebook, we access this model and test it with data the model has never seen before.</p>

<p>&nbsp;</p>

<h1>Conclusion</h1>
<p>Now we have a working Image Classification Program using a Convolutional Neural Network. This model can be edited to take in almost any image. In the future, I will be recreating this project by implementing the mathematics and algorithms from scratch. Thank you for your time and interest in this project!</p>
