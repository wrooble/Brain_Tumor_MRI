# This is my project Brain_Tumor_MRI in TF
## Data
I used dataset from kaggle website: https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset/data

The original data are in directory kaggle/input and is splitted into Training and Testing subset.
In those subsets data are in 4 directories containing MRI images of brains with glioma, meningioma, pituitary tumor and healthy ones.
## Preprocessing
In the preprocessing section, I used a function that found the edges of the brain in the images, cropped out this section and scaled it to 256 by 256 pixels.
The processed images were saved in the kaggle/working/resized_256 folder.
## Model
I created a model taking images in size (256,256,1), consisting of 6 alternating Conv2D and MaxPooling layers, a Flatten layer, a Dense layer with ReLU activation and a Dense layer with Softmax activation.
As output, it returned a vector of 4 probabilities of belonging to a given class.
On the test dataset, my model achieved an accuracy of 98% and it's saved in kaggle/working/model directory.
