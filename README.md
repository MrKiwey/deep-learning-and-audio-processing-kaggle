### Introduction

Systems able to recognize sounds directly from audio recordings are widely applicable. In this project,
you’ll attempt to create an audio tagging system by extracting audio clip image representations and then
using computer vision-based classification models. You can consider constructing your system using a
relatively large-scale competition data set and then evaluate it on its ability to recognize and distinguish more specialized sounds on locally generated recordings.

### Goals

1. Investigate and construct models for automatic audio tagging of noisy recordings.
2. Adapt this to smaller data sets of audio recordings, either by using a setup motivated by your
above findings or by transfer learning.
3. Construct an audio tagging application.

### Methods and materials

To achieve Goal 1 of the project, you can, for example, use the FSDKaggle2018 used in the Freesound
General-Purpose Audio Tagging Challenge on Kaggle. There are 41 categories of audio clips, and the
goal is to classify each clip. For the second objective, you can look for a data set on your own or
construct one yourself.

As part of the project, you should investigate ways to do data augmentation for audio.
You’ll make use of a variety of Python audio libraries, e.g., librosa. You should also look into fastxtend, a library built on top of fastai. To construct the application, you’re free to use any solution you know or want to investigate. A natural starting point is the deployment solutions used in the fastai course.

Consider not converting audio to images but instead setting up an audio classification framework that
operates on audio representations of the data.

## Our work

[This](https://towardsdatascience.com/audio-deep-learning-made-simple-sound-classification-step-by-step-cebc936bbe5) is the article we used for the first part in the notebook. We tried to replicate the work from the article, but got stuck somewhere with tensors. After much trying and failing, we decided to take the easy way out and just create mel-spectograms and use fastai to perform training on the pictures. You can find the code where we generated spectograms [here](https://github.com/MrKiwey/audio-processing-create-spectograms).

We used the FSDKaggle2018 dataset used in the Freesound General-Purpose Audio Tagging Challenge on Kaggle.

After creating the spectograms and importing them into Kaggle, we could use this notebook to perform machine learning on them, producing a model. Because of our time spent trying to create a model a different way, we were not able to do a lot of preprocessing on the data. Therefore the accuracy of our model is quite low, around 75%. Although, the biggest flaws in the model are on sounds that are quite similar. So it is understandable that it gets these wrong sometimes. If we were to work further with our model, this would be a point of interest. 

## Resources

Howard, J. and Gugger, S. (2020), *Deep Learning for Coders with Fastai and Pytorch: AI Applications Without a PhD* https://books.google.no/books?id=xd6LxgEACAAJ

Ketan Doshi (2021), <i>Audio Deep Learning Made Simple: Sound Classification, Step-by-Step </i>
https://towardsdatascience.com/audio-deep-learning-made-simple-sound-classification-step-by-step-cebc936bbe5
