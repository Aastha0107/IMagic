# IMagic : Photography Assistant
IMagic is a photography assistant which helps in improving quality of images by removing noise, enhancing lightning and resolution. This project addresses common challenges faced by non-professional photographers, such as noise, poor lighting, and low image quality. Basically, this model helps to enhance images and make good results available to everyone regardless of their technical expertise in photography.
IMagic includes three core functionalities:
 1. Noise removal - Removes noise from the images
 2. Light enhancement - Improves lightning (brightness) of images for better visibility.
 3. Resolution enhancement - Improves overall resolution of the image (not included in the final pipeline)
This project demonstrates the practical application of machine learning in photography, offering a user-friendly solution for enhancing photo quality.
Here, repository consists of four notebooks -
### Noise Removal
The architecture includes convolutional layers that learn to distinguish noise from important image features. 
##### 1. Data preprocessing :
Input consists of clean images of size 256x256 RGB images with 3 Channels. Preprocessing includes normalizing images to standardize pixel values between 0 and 1 and also includes resizing to 256x256 if needed.
##### 2. Model training :
Model is trained on about 25k images.Firstly any one of three noises(gaussian,salt-paper,speckle) is added to input images randomly. The model uses convolutional filters to extract noise patterns and remove them, producing a cleaner version just like the input image.
##### 3. Output :
Output includes clean images that closely resembles with input clean images.
### Light Enhancement 
An encoder-decoder architecture, incorporating skip connections, is used which is a robust and effective design for tasks like image enhancement. The model adjust image pixel intensity dynamically while preserving the natural look of the image.
##### 1. Data preprocessing :
Input consists of clean images of size 256x256 RGB images with 3 Channels. Preprocessing includes normalizing images to standardize pixel values between 0 and 1 and also includes resizing to 256x256 if needed.
##### 2. Model training :
Model is trained on about 3k images including images of different lightning to ensure model is trained images of various exposures.The model analyzes the image to detect underexposed regions. It adjusts brightness levels using learned transformations.
##### 3. Output :
Output includes images with proper lightning resembling ground truth images
### Resolution Enhancement
The architecture includes U-Net style auto encoder.This model upscale images while preserving important details and reducing blurriness.
##### 1. Data preprocessing :
Input consists of clean images of size 256x256 RGB images with 3 Channels. Preprocessing includes normalizing images to standardize pixel values between 0 and 1 and also includes resizing to 256x256 if needed.
##### 2. Model training :
Model is trained on about 700 images
##### 3. Output :
Output of this includes images with better resolution (reduced blur) compared to input low resolution images.
### Final Pipeline
In final pipeline all these three models are deployed and loaded along with their summary. However, resolution model is not working efficiently in the pipeline might be due to compatibility issues. So, images are enhanced with noise removal and light enhancement models.
###  Final Testing Dataset
This includes the images on which final pipeline is tested.
### FINAL DELIVERABLE
Final outcome of this project includes denoised image with better lightning. However in the outputs processed images are also shown.
### TECH STACK
#### Programming Language
- **Python** - used as core language
#### Libraries
- **TensorFlow** - Core library for building and training deep learning models
- **OpenCV** - Image processing and manipulation
- **MatplotLib** - Visualization of data and results
- **Numpy** - Numerical computations and array handling
- **Pandas** - Data manipulation library
- **Keras** - High-level neural networks API running on top of TensorFlow
- **tqdm** - Displays progress bars for iterative tasks
### Environment
Jupyter Notebook or Google Colab for running the notebook


This README provides an overview of the IMagic project, including the description of all three models deployed in the final pipeline and tech stack required for it. It aims to be informative for viewers and collaborators referring to this repository.
  
  
