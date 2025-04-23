# Audio-Visual Emotion Detection with eNTERFACE and Crema-D Datasets

## Overview
This project explores audio-visual emotion detection using the **eNTERFACE** and **Crema-D** datasets. My approach involves combining audio and visual data through a series of preprocessing techniques and fusion strategies to enhance multimodal emotion recognition.

## Data Preprocessing and Fusion Strategies

### Dataset: eNTERFACE or Crema-D
I selected the **eNTERFACE** dataset to provide both audio and visual data for emotion recognition tasks. The following preprocessing steps were used to manage multimodal inputs effectively:

1. **MFCC and Video Frames (with Image Representation)**
   - Extracted **Mel-frequency cepstral coefficients (MFCCs)** from audio, representing crucial audio features.
   - Combined these MFCC frames sequentially with video frames to form a unified input sequence for multimodal learning.

2. **Mel Spectrograms and Video Frames (with Image Representation)**
   - Extracted **Mel spectrograms** from audio, showcasing frequency-based features of the audio input.
   - Sequentially combined these spectrogram frames with video frames for a time-aligned audio-visual representation.

3. **Single-Mode Inputs (Audio or Video Only)**
   - Processed individual inputs using **only MFCC frames**, **only Mel spectrogram frames**, or **only video frames**, with each in image format.
   
These preprocessing techniques allow me to test both **unimodal** and **multimodal** models, highlighting the value of cross-modal feature representation in emotion detection tasks.

### Open Source Code for Loading eNTERFACE Dataset
For loading the **eNTERFACE** dataset, I recommend using this [official dataset link](https://enterface.net/enterface05/main.php?frame=emotion) for downloading and dataset handling.

## Fusion Strategies

To enhance feature alignment in multimodal data, I applied six optimized **fusion strategies** that capture spatial and temporal relationships, allowing for a more accurate recognition of emotions. The key fusion methods used are:

- **Early Fusion**: Combines audio and video data at the input layer, allowing both modalities to influence initial feature extraction.
- **Late Fusion**: Merges data at the classification layer, utilizing independently extracted features from each modality.

These fusion strategies contribute to more robust multimodal emotion recognition by integrating dynamic audio-visual data.

## Pre-trained Model

I utilized a pre-trained **VideoMAE encoder** model for multimodal sequence analysis, specifically the model fine-tuned on Kinetics-400. Here are the model details:
- Repository: [VideoMAE](https://github.com/innat/VideoMAE)
- Pre-trained Model Download: [TFVideoMAE_L_K400_16x224_FT](https://github.com/innat/VideoMAE/releases/download/v1.1/TFVideoMAE_L_K400_16x224_FT)

The **VideoMAE encoder** is based on masked autoencoders and is designed to capture key feature representations from both audio and video data for emotion recognition.

## Contact
For any inquiries, please reach out to:
- [mohammed.ghanemi@tum.de](mailto:mohammed.ghanemi@tum.de)
- [mohammed.ghanemi@iav.de](mailto:mohammed.ghanemi@iav.de)

---

## License
This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for more details.
