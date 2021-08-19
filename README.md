# tl-image-classification

The aim of this project is to be able to perform image classification on land use features through transfer learning.

The dataset can be found [here](http://weegee.vision.ucmerced.edu/datasets/landuse.html).

## Changelog (YY/mm/dd)

### 2021/08/19
- EfficientNet and VGG16 models were added. EfficientNet has 89% validation accuracy while VGG16 has 81%.
- The training time per epoch is displayed and can therefore be a tentative marker of model efficiency in addition to the test accuracy.
- Since we intend to create an end-user application, we have to convert a model to .tflite format for an Android application. From here we can run the model through Firebase. In this case we used the ResNet50 model as it has 89% test accuracy while being relatively fast. Using MobileNet or EfficientNet could be a good choice as well.

### 2021/08/16
- We also trained the data on the MobileNetV2 and InceptionV3. 
- We found that MobileNet trains much faster and has 60% accuracy (expected, as it is a lightweight deep-learning model)
- However, InceptionV3 had only 40% accuracy with comparable training time.
- Benchmarking and analysis to come soon.

### 2021/08/15

- The addition of Singapore land use images is mostly complete, and hopefully will improve training in the Singapore context.
- Object detection can be done after image classification. The data would come in useful for a comprehensive data analysis of Singapore land usage.
- The model is retrained on some Singapore images and the validation accuracy is 92.92%.
- The original UCMerced_LandUse dataset folder is added as a fallback.

### 2021/08/10

- Decided to go with sampling images from a Folium map. These images would be useful especially if we were to conduct the classification in the Singapore context.
- Test accuracy stands at about 89% which is close to the validation accuracy 
- Added the dataset folder to the repository. Singapore image augmentation done slightly and still in progress.

### 2021/07/11

- Added saved model (~90% accuracy)

### 2021/07/08

- Initialised Git repository
- Connected Colab notebook

## Acknowledgements

Yi Yang and Shawn Newsam, "Bag-Of-Visual-Words and Spatial Extensions for Land-Use Classification," ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems (ACM GIS), 2010.
