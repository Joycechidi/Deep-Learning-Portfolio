# Table of Contents

1. Installation
2. Project Motivation
3. File Descriptions
4. Results
5. Licensing, Authors, and Acknowledgements

## Installation
Because I worked on Google collaboratory which has most of the PyTorch and Machine Learning libraries pre-installed, I didn't have to install any of the libraries used in this project.
If you are working on your local machine, you need to install the following: 
os, 
pillow, 
torch, 
optim, 
requests, 
torchvision

The code should run with no issues using Python versions 3.7

## Project Motivation
For this project, I wanted to understand the following:
1. How to transfer the style and features of an artistic image to my personal photo based on the technical paper, **Image Style Transfer Using Convolutional Neural Networks, by Gatys in PyTorch.
2. How a pre-trained model (VGG19) and a neural network can help me achieve this process
3. What my target image will look like at the end of running algorithm and 2000 iterations


## File Descriptions
There are 2 jupyter notebooks available here to showcase work related to the above project motivations. The difference between the 2 files are:
each notebook has a different style image. In one notebook I used 2000 iterations to update the target image while in the 2nd notebook I used 5000 iterations for updating the content image.
Markdown cells were used in the notebook to explain the job of the each code and to assist in walking through the thought process for individual steps.

There is a photo showing my result.
However, I have not included the two images used in this project. Please feel free to use your own images.

## Results
The results of the code are images showing a transfered style towards the end of the code.
Results can also be found as image files in this repository.

## Licensing, Authors, Acknowledgements
The thought process for the code: Credit: Udacity Deep Learning Nanodegree
### Image Credits: 
Joyce Chidiadi

21st Century Art Movement: [https://medium.com/predict/the-21st-century-art-movement-what-is-it-a5db9dcc1d97]

Torsion And Rotation Movement Art vector image: [https://www.vectorstock.com/royalty-free-vector/torsion-and-rotation-movement-art-vector-6600711]

Feel free to use the code here but <__please use__> your own images.
