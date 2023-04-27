# Dense_Video_Captioning

# Introduction
This project aims to generate captions for videos by associating each time step with a caption instead of generating a single caption for the entire video. The project uses a dense video captioning model that generates multiple captions for each time step, which are then scored and ranked to produce a final caption for the time step.

# MSVD Dataset
The Microsoft Research Video Description Corpus (MSVD) is a dataset of short videos, each accompanied by a set of textual descriptions. For this project, we have used dataset consists of 1450 training videos and 100 testing videos, with an average duration of 10 seconds per clip. Each video has at least one caption, and there are a total of 70,028 captions in the dataset.

# Model
Proposed architecture comprises an event proposal module, an EfficientNet B7 network for feature extraction from sampled frames, and BiLSTM encoder and LSTM decoder for captioning. BILSTM encoder effectively utilizes both past and future contexts from the video for generating captions.This model captures temporal information and dynamics of video and generates caption in real time. The PySceneDetect API is used to detect scenes in the video. API computes the difference of pixels across all channels in an HSV frame and detects scene change by comparing the resulting difference to a given threshold. Further EfficientNetB7 neural network is used for extracting features as it gives better accuracy and has considerably less number of parameters. Model employing a BiLSTM and LSTM encoder-decoder architecture is presented. The data demonstrate that our dense video captioning module performs well on the BLEU@1,2,3,4 and METEOR metrics.

# Installation
To install the necessary dependencies, run the following command: pip install -r requirements.txt
# Data Format
The dataset is available in two formats: (1) MP4 video files and (2) a .json file containing the captions for each video id. The video files are named according to their unique ID.
VideoID: a unique ID for each video
Description: the text description of the action or event in the video during the specified time period

# Usage
Download the MSVD dataset.
To convert into features run the extract_features.py file as python extractFeaturesEfficientNetB7.py
Run train.py for local training or use the Efficient NET B7_ modeltrain_.ipynb notebook

# Model
# Training Architecture
![image](https://user-images.githubusercontent.com/49709163/234733154-b97b3fd8-738a-45ee-91e9-4e50247bfe5e.png)
 # Encoder Model
 ![image](https://user-images.githubusercontent.com/49709163/234733784-0856ebae-b9aa-4093-89ed-86a95458aa68.png)
# Decoder Model
![image](https://user-images.githubusercontent.com/49709163/234733933-30f038da-6db0-4631-9819-58d1539de3e1.png)

# Metric
This is the graph of epochs vs metric. The metric used is accuracy.![image](https://user-images.githubusercontent.com/49709163/234734018-f5a6d1eb-5668-4dea-8bf8-17766cbb7679.png)
# Loss
This is the graph of epochs vs loss. The loss used is categorical crossentropy.![image](https://user-images.githubusercontent.com/49709163/234734122-dacde4ed-de74-4c8c-b584-2a3194f093a4.png)












