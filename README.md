# Naive-Bayes-Pixel-Level-Image-Segmentation

Implementation of a naive Bayes algorithm for Image segmentation trained with The Oxford-IIIT Pet Dataset.

Dataset Link: https://www.robots.ox.ac.uk/~vgg/data/pets/

## Test Results
### Best result
![Comparison of two images with best results](https://github.com/Jon-Lein/Naive-Bayes-Pixel-Level-Image-Segmentation/blob/main/Some%20Results/Best_result.png)

The solid background of this image produced one of the best results from my testing set. 

### Background Noise
![Comparison of two images with best results](https://github.com/Jon-Lein/Naive-Bayes-Pixel-Level-Image-Segmentation/blob/main/Some%20Results/Best_result.png)

Many of the images had little sections of the background that the prediction was very close between the dog and background class that were incorrectly classified as dog pixels. An algorithm could be applied to remove the small clusters of pixels and keep only the large sections.


