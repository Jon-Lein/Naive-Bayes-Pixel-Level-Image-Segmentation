# Naive-Bayes-Pixel-Level-Image-Segmentation

Implementation of a naive Bayes algorithm for Image segmentation trained with The Oxford-IIIT Pet Dataset.

Dataset Link: https://www.robots.ox.ac.uk/~vgg/data/pets/

## Test Results
### Best result
![Comparison of two images with best results](https://github.com/Jon-Lein/Naive-Bayes-Pixel-Level-Image-Segmentation/blob/main/Some%20Results/Best_result.png)

The solid background of this image produced one of the best results from my testing set. 


### Background Noise
![Comparison of two images with results containing some image noise](https://github.com/Jon-Lein/Naive-Bayes-Pixel-Level-Image-Segmentation/blob/main/Some%20Results/Some_Noise.png)

Many of the images had little sections of the background that the prediction was very close between the dog and background class that were incorrectly classified as dog pixels. An algorithm could be applied to remove the small clusters of pixels and keep only the large sections.


## Bad Lighting
![Comparison of two images with results containing some bad lighting](https://github.com/Jon-Lein/Naive-Bayes-Pixel-Level-Image-Segmentation/blob/main/Some%20Results/Bad_Lighting.png)

The data set and test images I used didn't have consistant lighting and many times shadows were able to darken the Samoyd's fur just enough to catagorize it as background pixels.


## Background Colors
![Comparison of two images with results containing yellow flowers in the background](https://github.com/Jon-Lein/Naive-Bayes-Pixel-Level-Image-Segmentation/blob/main/Some%20Results/Flowers.png)

The training data set lacked some colors in the background that appeared in testing images. These yellow flowers in the background were on the boundry between the background and dog classes. The lighting on the edges of them lightened the pixels enough to push them into the dog class. There was little to no yellow present in the training data set so the algorithm didn't have a clear idea where to classify them. The lightness of the color was closer to the white dog pixels than the typically darker background pixels.


## Worst Result
![Comparison of two images with results containing yellow flowers in the background](https://github.com/Jon-Lein/Naive-Bayes-Pixel-Level-Image-Segmentation/blob/main/Some%20Results/Worst_Result.png)

I wasn't expecting any good results with this image in the testing set. As this algorithm relies only on color data, the bright white background would confuse the algorithm. This algorithm wouldn't be able to get good results on images like this with any amount of tweaking or added testing data.

## Conclusions
This algorithm provided better results than I expected given the test data set I used was not as uniform as the dataset generated in the paper the algorithm is based on. The algorithm could take a moderate amount of images with varying background and lighting and segment images with clean uniform backgrounds very well. Even images with more noisey backgrounds could produce decent results with some minor misclassifications. The performance of the algorithm was fast enough that additional computer vision algorithms could be used to improve the results and still produce the result in a reasonable amount of time. 
