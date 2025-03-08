# Video_classification

## Information

<b>Background :</b> The CNN LSTM architecture involves using Convolutional Neural Network (CNN) layers for feature extraction on input data combined with LSTMs to support sequence prediction.

CNN LSTMs were developed for visual time series prediction problems and the application of generating textual descriptions from sequences of images (e.g. videos). Specifically, the problems of:

Activity Recognition: Generating a textual description of an activity demonstrated in a sequence of images

Image Description: Generating a textual description of a single image.

Video Description: Generating a textual description of a sequence of images.

Applications: Applications such as surveillance, video retrieval and human-computer interaction require methods for recognizing human actions in various scenarios. In the area of robotics, the tasks of autonomous navigation or social interaction could also take advantage of the knowledge extracted from live video recordings. Typical scenarios include scenes with cluttered, moving backgrounds, nonstationary camera, scale variations, individual variations in appearance and cloth of people, changes in light and view point and so forth. All of these conditions introduce challenging problems that can be addressed using deep learning (computer vision) models.

## Dataset

<b>Dataset :</b> This dataset consists of labelled videos of 6 human actions (walking, jogging, running, boxing, hand waving and hand clapping) performed several times by 25 subjects in four different scenarios: outdoors s1, outdoors with scale variation s2, outdoors with different clothes s3 and indoors s4 as illustrated below.



All sequences were taken over homogeneous backgrounds with a static camera with 25fps frame rate. The sequences were downsampled to the spatial resolution of 160x120 pixels and have a length of four seconds in average. In summary, there are 25x6x4=600 video files for each combination of 25 subjects, 6 actions and 4 scenarios. For this mini-project we have randomly selected 20% of the data as test set.

Dataset source: https://www.csc.kth.se/cvap/actions/

<b>Methodology:</b>

When performing image classification, we input an image to our CNN; Obtain the predictions from the CNN; Choose the label with the largest corresponding probability

Since a video is just a series of image frames, in a video classification, we Loop over all frames in the video file; For each frame, pass the frame through the CNN; Classify each frame individually and independently of each other; Choose the label with the largest corresponding probability; Label the frame and write the output frame to disk

Refer this Video Classification using Keras for complete understanding and implementation example of video classification.
