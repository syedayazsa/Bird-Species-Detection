# Bird Species Detection:

Built a deep-learning model to classify 225 bird species having 31316 training images, 1125 test images(5 per species) and 1125 validation images.

Images were gather from internet searches by species name. Once the image files for a species was downloaded they were checked for duplicate images using a python duplicate image detector program I developed. All duplicates detected were deleted in order to prevent their being images common between the training, test and validation sets.

After that the images were cropped so that the bird occupies at least 50% of the pixel in the image. Then the images were resized to 224 X 224 X3 in jpg format. The cropping ensures that when processed by a CNN their is adequate information in the images to create a highly accurate classifier. All files were also numbered sequential starting from one for each species. So test images are named 1.jpg to 5.jpg. Similarly for validation images. Training images are also numbered sequentially with "zeros" padding. For example 001.jpg, 002.jpg ….010.jpg, 011.jpg …..099.jpg, 100jpg, 102.jpg etc. The zero's padding preserves the file order when used with python file functions and Keras flow from directory.

The training set is not balanced, having a varying number of files per species. However each species has at least 100 training image files. This imbalanced did not effect my kernel classifier as it achieved over 98% accuracy on the test set.

One significant imbalance in the data set is the ratio of male species images to female species images. About 80% of the images are of the male and 20% of the female. Males typical are far more diversely colored while the females of a species are typically bland. Consequently male and female images may look entirely different .Almost all test and validation images are taken from the male of the species. Consequently the classifier may not perform as well on female specie images.

![Image](https://i.ibb.co/WKWdVnH/Screenshot-2021-05-06-at-5-39-04-PM.png)


## Tools/Libraries Used:
```
Keras
TensoFlow
Pandas
Numpy
Keras
Matplotlib
```



## Results: 
  - Training Accuracy: 90.5% | Training Loss: 0.3317
  - Validation Accuracy: 94.63% | Validation Loss: 0.1936


<img align="left" alt="img" src="https://i.ibb.co/y6MMc3s/Screenshot-2021-05-06-at-5-41-21-PM.png" width="350" height="260" />
<img align="right" alt="img" src="https://i.ibb.co/pb4SVWz/Screenshot-2021-05-06-at-5-41-08-PM.png" width="350" height="260" />


