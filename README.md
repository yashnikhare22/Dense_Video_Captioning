# Dense_Video_Captioning

# Introduction
This project aims to generate captions for videos by associating each time step with a caption instead of generating a single caption for the entire video. The project uses a dense video captioning model that generates multiple captions for each time step, which are then scored and ranked to produce a final caption for the time step.

# MSVD Dataset
The Microsoft Research Video Description Corpus (MSVD) is a dataset of short videos, each accompanied by a set of textual descriptions. For this project, we have used dataset consists of 1450 training videos and 100 testing videos, with an average duration of 10 seconds per clip. Each video has at least one caption, and there are a total of 70,028 captions in the dataset.

# Model
Proposed architecture comprises an event proposal module, an EfficientNet B7 network for feature extraction from sampled frames, and BiLSTM encoder and LSTM decoder for captioning. BILSTM encoder effectively utilizes both past and future contexts from the video for generating captions.This model captures temporal information and dynamics of video and generates caption in real time. The PySceneDetect API is used to detect scenes in the video. API computes the difference of pixels across all channels in an HSV frame and detects scene change by comparing the resulting difference to a given threshold. Further EfficientNetB7 neural network is used for extracting features as it gives better accuracy and has considerably less number of parameters. Model employing a BiLSTM and LSTM encoder-decoder architecture is presented. The data demonstrate that our dense video captioning module performs well on the BLEU@1,2,3,4 and METEOR metrics.

# Installation
To install the necessary dependencies, run the following command: pip install -r requirements.txt
