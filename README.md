# Image-Captioning-using-Show-Attend-and-Tell-paper
The goal is to generate a caption in English language, given an image

* The model architecture is inspired by the "Show, Attend and Tell" (https://arxiv.org/pdf/1502.03044.pdf) paper.

* The dataset used is Flicker30K and images used are 6000 and its associated 30k captions which is 5 captions per image.
* The dataset is having varieties of images and hence if more data is used for training, predictions could have been much better, but that need
  heavy GPU.
* More than 30% captions are gramatically incorrect and to some extent I have cleaned them using Grammerly software.
* The CNN architecture used is Inception which has appx 24M parameters. I have tried VGG-16 which has appx 134M parameters, but the
  predictions were almost similar and hence I didnt used the VGG-16.
* The Decoder architecture is based on Show Attend and Tell paper but the loss is not converging less than 0.57 even after 200 epochs and
  hence need to end the loss at 0.57.
* The results are not at par Bahdanau Attention Decoder.
* Played with batchsize of 32 and 64, but both giving appx same results and I have choosen 64 as it has less iterations per epoch.
* Have used Greedy search and Beam Search with 5 and 7 predictions.
* Some predictions are repetitive and this behaviour is not understandable, tried to solve but coud'nt due to lack of expertise.
* Thanks to Tensorflow blog on this topic through which this woud'nt be possible.
