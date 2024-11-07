# Audio-Visual Emotion Detection with eNTERFACE Dataset

## Overview
This project explores audio-visual emotion detection using the **eNTERFACE** dataset. The approach involves combining audio and visual data through a series of preprocessing techniques and fusion strategies to enhance multimodal emotion recognition.

## Data Preprocessing and Fusion Strategies

### Dataset: eNTERFACE
The **eNTERFACE** dataset was selected to provide both audio and visual data for emotion recognition tasks. The following preprocessing steps were used to manage multimodal inputs effectively:

1. **MFCC and Video Frames (with Image Representation)**
   - Extracted **Mel-frequency cepstral coefficients (MFCCs)** from audio, representing crucial audio features.
   - Combined these MFCC frames sequentially with video frames to form a unified input sequence for multimodal learning.
   - 

2. **Mel Spectrograms and Video Frames (with Image Representation)**
   - Extracted **Mel spectrograms** from audio, showcasing frequency-based features of the audio input.
   - Sequentially combined these spectrogram frames with video frames for a time-aligned audio-visual representation.

3. **Single-Mode Inputs (Audio or Video Only)**
   - Processed individual inputs using **only MFCC frames**, **only Mel spectrogram frames**, or **only video frames**, with each in image format.
   
These preprocessing techniques allow for testing both **unimodal** and **multimodal** models, highlighting the value of cross-modal feature representation in emotion detection tasks.

## Fusion Strategies

To enhance feature alignment in multimodal data, we employed six optimized **fusion strategies** that capture spatial and temporal relationships, allowing for a more accurate recognition of emotions. The key fusion methods used are:

- **Early Fusion**: Combines audio and video data at the input layer, allowing both modalities to influence initial feature extraction.
- **Late Fusion**: Merges data at the classification layer, utilizing independently extracted features from each modality.

These fusion strategies contribute to more robust multimodal emotion recognition by integrating dynamic audio-visual data.

---

## Model Information
This project utilizes a pre-trained **VideoMAE encoder** for multimodal sequence analysis, leveraging masked autoencoders to capture feature representation from both audio and video data.

## Contact
For any inquiries, please reach out to [mohammed.ghanemi@tum.de] or [mohammed.ghanemi@iav.de]


---

## Citation
If you find this repository helpful, please consider citing our work.

