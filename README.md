# Classifying Human Voices
In this project, I tried to classify human voices based on their genders and emotions.

## Dataset
This was a class project and every one in the class contributed in gathering the data. Unfortunately, I am not allowed to share the dataset online.
However, I can provide some details about the dataset I used. Eeach one of us had to record 10 different sentences with 4 different emotions for at least 4 differnt people.

Sentences: (The original sentences are in Persian, I have translated them below)
1. Hello to you. 2. Thank you. 3. You worked hard. 4. I became very happy. 5. It is obvious. 6. You are right. 7. How are you. 8. It is kind of you. 9. Definitely so. 10. That is really great.

Emotions:
1. Anger 2. Joy 3. Sadness 4. Neutral

* Audio Files: Their names only consists of voice IDs. The details about these files are written in an excel file.
* Excel: details about each audio file is provided in an excel file. The columns are named like this: emotionID, textID, sex, age, voice ID

## Feature Extraction
I used the following  methods to extract the features from audio files. The number in front of each case shows the number of features that each method provides. 
- Zero Crossing Rate: Average (1), Variance (1)
- RMS: Average (1), Variance (1)
- Spectral Centroid: Average (1), Variance (1)
- Spectral Bandwidth: Average (1), Variance (1)
- Spectral Roll Off: Average (1), Variance (1)
- Chroma STFT: Average (1), Variance (1)
- Tonality: Average (6), Variance (6)
- MFCC: Average (20), Variance (20)
- Mel Spectrogram: Average (20), Variance (20)
I concatenated all of the extracted features, and saved the whole dataset as a numpy array. 

**IMPORTANT NOTE:** When I wanted to classify the audiofiles, I would slice dataset to pick different features. 
## Classifying
SVM and Random forests were used for classifying audio files based on emotions and genders.
