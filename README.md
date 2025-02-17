# Speaker Recognition System with Bi-Directional LSTM

This  project focused on speaker verification using a custom Bi-Directional LSTM-based model. The model was trained and tested on an audio dataset of 50 unique speakers, leveraging advanced audio processing techniques to extract meaningful features and achieve effective speaker classification.

# Dataset Description 
* Dataset link: https://www.kaggle.com/datasets/vjcalling/speaker-recognition-audio-dataset
* The dataset used in this project is the Speaker Recognition Audio Dataset from Kaggle. It contains audio recordings of 50 unique speakers.

# Project Overview

## Audio Processing
* The first step involved preparing the raw audio data
* Loading Audio Files: Each recording from the dataset was loaded for processing. 
* Performed Noise reduction, Normalization, applied pre-emphasis filter to each audio recording
* Padding: Audio recordings were padded to the same length to ensure consistent input shapes for model training.

## MFCC Feature Extraction
* To transform the raw audio signals into meaningful features, Mel-Frequency Cepstral Coefficients (MFCC) were extracted:
* MFCC features represent the short-term power spectrum of sound, calculated on a Mel scale. This feature extraction technique is widely used in speech recognition and speaker verification as it captures the unique characteristics of a speaker's voice.
* Feature Extraction: For each audio recording, 40 MFCC features were extracted. These features were then stacked into sequences and padded to ensure uniform shape across all samples.
  
## Model Building
* The project utilized a Bi-Directional LSTM model:
* LSTM (Long Short-Term Memory): A type of recurrent neural network (RNN) that captures long-term dependencies in sequential data.
* Bi-Directional Layer: Processes sequences in both forward and backward directions, helping capture context from both past and future frames.
* The model was built with multiple hidden layers to learn complex patterns in the MFCC feature sequences.
  
## Model Training and Evaluation
* Training: The model was trained for 30 epochs using the training dataset.
* Loss Function and Optimization: Standard categorical cross-entropy loss was used, optimized with the Adam optimizer.
* Validation: Accuracy and loss were tracked during training to monitor overfitting and performance.

## Model Evaluation
* The trained model was evaluated on a test set to assess its performance:
* Test Accuracy: 0.8249
* Precision: 0.8530
* Recall: 0.8249
* F1 Score: 0.8217
* These results indicate that the model performed well in distinguishing speakers from the dataset with a strong balance between precision and recall.

