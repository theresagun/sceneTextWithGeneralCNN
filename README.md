# sceneTextWithGeneralCNN
Holistic Identification of Scene Text with a General Image Classification CNN

A motivating factor behind utilizing whole word
recognition is to have the CNN more accurately model the
way the human brain interprets a word. A 1997 psychology
study suggests that the human brain reads words by
identifying clusters of shapes and associating their meaning
with a word, rather than identifying each character of a word
sequentially. This type of recognition is what scientists refer
to as “holistic visual information” and differs from the
“preliminary letter recognition” that is commonly referred
to in the text recognition CNN field.
Our objective is to demonstrate that a whole word
recognition system can be built by training an already
established image recognition network with pictures of
words. To our knowledge, whole word recognition has only
been attempted using a CNN that is specialized for text
recognition.
Our model uses AlexNet along with a self-compiled
database to create a more accurate and intuitive text
recognition artificial intelligence system. We decided that
implementing our research on a known network would
eliminate unknown variances that may occur in a
custom-built network for image recognition. Because
AlexNet has been cited in many papers and corroborated by
many sources, we felt as though it was suited for our
research.
AlexNet is a deep convolutional neural network
originally made to classify 1.2 million images in the
ImageNet database into a thousand different classes.
The initial architecture of the network consists of eight
layers: five convolutional and three fully-connected layers.
In addition, there are pooling layers incorporated into the
CNN. A visual of the network can be viewed in figure 2.
One major difference between whole word recognition
and character by character text recognition is the number of
outputs. Character by character recognition usually has less
than 100 outputs, depending on how many unique
characters can be recognized. On the other hand, whole
word recognition has over 150,000 potential outputs in the
English language. We would need several hundred
images of each word to use our model to identify every
word. With the current technology available, it would be
nearly impossible to create a complete whole word
recognition network.
To account for this issue, we started with eleven image
classes, each consisting of approximately two hundred
images. Specifically, we are focusing on words that appear
on traffic signs because these contain the variety of text that
we are looking for and they can be found through a simple
online search. This project is in no way limited to solely
being a street sign recognition network. We created our own
datasets by hand, which explains the low number of images
in each. The intent for this research is to show that whole
word recognition can be performed on a larger scale without
the need for a dedicated word recognition CNN.
When compiling our dataset, we took several measures to
ensure that we were training our CNN to recognize words
by shape more so than other characteristics. First, we
cropped the images so that only the word to be identified
was present. This would ensure the shape of the sign would
not be taken into account when recognizing words. We
ensured that our dataset included signs with various fonts
and a mix of light text on a dark background and dark text
on a light background. We also converted every image to
grayscale so that the CNN would not base its output off of
color.
Rather than creating individual labels for each image in
our dataset, we grouped our images into folders so that each
folder was its own image class. After preprocessing and
grouping our images, we uploaded them onto our computer
that was provided for us by NVIDIA. We chose to make and
train our model using DIGITS, which is a user interface for
neural networks and works with the GPU that came with our
computer.
We decided to utilize DIGITS for our project because it
allows users to easily adjust aspects of AlexNet such as the
number of training epochs, learning rate, and dropout rate.
After uploading our dataset to DIGITS, we partitioned it
into training, testing, and validation sets. We trained several
models with our dataset, adjusting the different variables in
order to optimize results. DIGITS also has several tools,
such as a graphing feature, that allow us to visualize what
our model looks like throughout the training process.
Because we were able to use a powerful GPU to train our
model and have a relatively small dataset of about two
thousand images, we were able to train each of our models
in about a minute.
