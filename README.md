# Multiclass classification with class imbalance
This group university project was focused on researching convolutional neural network training with class imbalance. Similar solutions were researched and it has been found that VGG16 and ResNet50 achieve the highest results on multiclass problems.

The dataset chosen for the project was Animals-10 dataset that may be accessed on [Kaggle](https://www.kaggle.com/datasets/alessiocorrado99/animals10/data). The dataset has been collected using Google Images and checked by a human, however, it does contain intentional errors to better simulate a real working environment for the trained model. It contains 10 classes


To balance the dataset we proposed two methods based on oversampling. It was required as oversampling the whole dataset at once was too RAM-consuming. The first method was to resize the images to 100x100 pixels and perform oversampling on the whole dataset. Then we resized the images to 224x224 (model input size both for VGG16 and ResNet50). The second method performed oversampling on batched data. 
Experiments showed that the second method performed better. 

We experimented with training on an imbalanced dataset which resulted in non-uniform error distribution, i.e. classes with more data were recognized much better than the classes with the least data. Oversampling fixed that behavior.

We trained both models from scratch and using transfer learning which gave better results. We tuned the parameters to maximize the accuracy. We achieved 89% accuracy on VGG16 and 97% accuracy on ResNet50. 


