# Synthetic-Microscopy-Images<br>

### Objective
The objective of this project is to provide a simple tool for those who work with atomic-resolution electron microscopy images to create artificial images of different crystal lattices. In this way, there is a possibility to produce hundreds to thousands of images of your lattice and you might change something in the regular lattice-like introducing defects, etc to study some physical and chemical phenomena. Having this said, one can use the synthetic dataset of images to develop a deep learning network to train a model and then test the model with experimental data.

### Introduction
The definition of the crystal categories might not be very accurate in this code, because depending on the crystal structure, orientation, and contrast of the atoms, there might be some overlapping of different categories. This can be further explored when one trains a deep learning model e.g. using vgg pretrained architect which I dedicate another repository for that. Therefore, this code is a guide for those who are interested in building their own lattices and they have to customize and test different parameters accordingly.  <br>
In the code, one can create images with different noise levels, introduce scanning distortion, change the atom size mimicking the atomic radii of elements in the material, change the contrast of the atoms to simulate the use of different detectors like HAADF or ABF, also the camera length might change the contrast of the atoms in the image. By the end, I have converted images to png format, with the type of uni8 and normalized to [0 , 1] range, only because of other tools I was using these images for. Of course, it is easy to save images in different formats. In some point, I have used cupy instead of numpy as it works better for parallel computing when you have access to multile core computation facility.  
The jupyter notebook file is called, random_lattice_dataset, a bit strange name, but it was just a conceptual idea to investigate different deep learning architecture like vgg, ResNet, Inception etc on high-resolution STEM images. That is why I just created some lattices to have some difference in their crystal structure.  

### Used Packages
To create the dataset, I have used the following packages:<br><br>
1- Hyperspy       version 1.7.3  <br>
2- temul-toolkit  version 0.1.7  <br>
3- Python         version 3.10.8 <br>
4- Pillow         version 9.4.0  <br>
5- Cupy           version 11.4.0 <br>

Please notice that it is always recommended to have short practice with hyperspy and temul packages, like what is a signal, or data structure types in hyperspy, or what one can do in temul package. Here is the link for the packages to get a deeper insight into their potential and use cases for the microscopy community. Many thanks to the developers of these open-source, powerful packages.   

https://hyperspy.org/hyperspy-doc/v1.6/index.html <br>
https://temul-toolkit.readthedocs.io/en/latest/index.html  <br><br>

In the end, I wish to get feedback on what should be improved or what can be added to give value to someone. As I am occupied with other things, I have not had enough time to go through the details and whether all images are ok or not.
