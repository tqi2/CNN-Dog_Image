# CNNs-Dog-Image-Project
[//]: # (Image References)

[image1]: ./result/me.png "me"
[image2]: ./result/bullterrier.jpeg "melike"
[image3]: ./result/trump.png "trump"
[image4]: ./result/greyhound.jpeg "trumplike"

# Overview
The second project for Udacity Deep Learning Nanodegree program. In this project, I explored state-of-the-art CNN models for classification, built a pipeline to process real-world, user-supplied dog images. Given an image of a dog, my model will identify an estimate of the canine’s breed. If supplied an image of a human, just for fun, my code will identify the resembling dog breed.

# Data
The training data for this project is located [here](https://s3-us-west-1.amazonaws.com/udacity-aind/dog-project/dogImages.zip). This dataset contains 133 different breeds of dogs and is already split into train, test, and validation sets. Place the training, testing, and validation datasets in the `dogImages` folder.

# Environment
Python: 3.6

PyTorch: 0.4.0

GPU: NVIDIA GeForce GTX 970M

Windows: 8.1

# Result
With the pretrained Resnet50, I used transfer learning on new dog image data, the models has 75% accuracy on test data for dog breed with only 5 epochs of training (took less than 10 mins). The final user app used the pretrained VGG16 as a dog detector, then used the tuned Restnet50 as dog breed classifier, for humans, I used OpenCV's implementation of Haar feature-based cascade classifiers to detect human faces in images.

I tried the app with a photo of myself, it showed I look like a Bull terrier and Trump looks like Greyhound.

![me][image1]

here is an example of a Bull terrier:

![melike][image2]

For Trump:

![trump][image3]

here is an example of a Greyhound:

![trumplike][image4]

# Deliverable
Check the [*dog_app.ipynb*](./dog_app.ipynb) for model with detail in code.

Check [*myphoto*](./myphoto) for the photos I tried with my app.
