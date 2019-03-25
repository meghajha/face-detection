
Before preceding into the face detection we need to know what Haar-like features and cascade classifiers are. Traditionally working with image intensities(using RGB) made the task of feature calculation computationally expensive. Then people started to talk about feature calculation based on Haar wavelets to reduce the cost of computation. Paul Voila and Michel Jones in 2001 used this concept and developed the Haar-like features. A Haar-like feature considers adjacent rectangular regions at a specific location in a detection window, sums up the pixel intensities in each region and calculates the difference between these sums. This difference is used to categorize the subsections of an image. For e.g in human face images, the region of eyes is darker than cheeks.

So when detecting an object in an image, the window of target size is moved over the input image and for each subsection of the image the Haar-like feature is calculated. This difference is then compared to the learned threshold that separates the object from non-objects.

The Haar-like features are weak learners or classifiers so large number of Haar-like features are necessary to classify images with higher accuracy. This is because one simple image can contain 180, 000+ Haar-like minute features. That’s why in Haar-like features are organized into something called classifier cascade to form a strong learner or classifier. Due to the use of the integral image, the Haar-like features can be calculated in very higher speed than the traditional approach.
