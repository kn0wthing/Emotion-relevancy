# Emotion-relevancy

In this experiment  tried to recognize emotion in short voice message. I will use 4 datasets with some english phrases: Ravee, Crema, Savee and Tess.

Dataset can be found in https://www.kaggle.com/dmitrybabko/speech-emotion-recognition-en

Datasets used in this project contains ~7 types of main emotions: Happy, Fear, Angry, Disgust, Surprised, Sad or Neutral

Meta-data regarding naming conventions:
Modality (01 = full-AV, 02 = video-only, 03 = audio-only).
Vocal channel (01 = speech, 02 = song).
Emotion (01 = neutral, 02 = calm, 03 = happy, 04 = sad, 05 = angry, 06 = fearful, 07 = disgust, 08 = surprised).
Emotional intensity (01 = normal, 02 = strong). NOTE: There is no strong intensity for the 'neutral' emotion.
Statement (01 = "Kids are talking by the door", 02 = "Dogs are sitting by the door").
Repetition (01 = 1st repetition, 02 = 2nd repetition).
Actor (01 to 24. Odd numbered actors are male, even numbered actors are female).


As dataset is limited, we performed data augmentation opeartions:
Noise injection
Stretching
Shifting
Pitching

I dont have any prior knowledge regarding speech features so using the recommended ones as features:
Zero Crossing Rate : The rate of sign-changes of the signal during the duration of a particular frame.
Energy : The sum of squares of the signal values, normalized by the respective frame length.
Entropy of Energy :The entropy of sub-frames’ normalized energies. It can be interpreted as a measure of abrupt changes.
Spectral Centroid : The center of gravity of the spectrum.
Spectral Spread : The second central moment of the spectrum.
Spectral Entropy : Entropy of the normalized spectral energies for a set of sub-frames.
Spectral Flux : The squared difference between the normalized magnitudes of the spectra of the two successive frames.
Spectral Rolloff : The frequency below which 90% of the magnitude distribution of the spectrum is concentrated.
MFCCs Mel Frequency Cepstral Coefficients form a cepstral representation where the frequency bands are not linear but distributed according to the mel-scale.

CNN Model with inspiration from resnet block is used.

For preprocessed dataset and model contact :)

Special thanks:
https://towardsdatascience.com/speech-emotion-recognition-with-convolution-neural-network-1e6bb7130ce3
https://www.kaggle.com/salmaneunus/a-basic-guide-to-speech-recognition
https://www.kaggle.com/dmitrybabko/speech-emotion-recognition-en
