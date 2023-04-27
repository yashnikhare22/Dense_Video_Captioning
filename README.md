# Dense_Video_Captioning

# Introduction
This project aims to generate captions for videos by associating each time step with a caption instead of generating a single caption for the entire video. The project uses a dense video captioning model that generates multiple captions for each time step, which are then scored and ranked to produce a final caption for the time step.

# Data
The project uses the ActivityNet Captions dataset, which consists of 20k videos of human activities, along with multiple annotations of temporal segments and their corresponding captions. The dataset is split into train, validation, and test sets.

# Model
The model architecture consists of a convolutional neural network (CNN) to encode the video frames and a recurrent neural network (RNN) to generate captions. The model uses a soft attention mechanism to attend to relevant parts of the video when generating each caption. The model is trained using a maximum likelihood objective.

# Installation
To install the necessary dependencies, run the following command: pip install -r requirements.txt
