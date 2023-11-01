[MEDIUM link](https://medium.com/@saipraneethk181200/action-recognition-from-video-frames-f309265d89ce)

# Action Recognition from Video Frames


## Overview

The process can be broken down into the following main steps:

1. **Setup and Dependencies**: 
   - Ensure you have Python installed. 
   - Key libraries required include TensorFlow (with TensorFlow Hub for feature extraction), OpenCV (for frame extraction from videos), and scikit-learn (for data splitting and SVM classifier training).

2. **Frame Extraction**:
   - Frames are extracted from input videos using OpenCV. Each video is broken down into its constituent frames, which are saved as individual images.

3. **Feature Extraction**:
   - Features are extracted from the frames using a pre-trained MobileNetV2 model from TensorFlow Hub. This model converts each image frame into a high-dimensional feature vector that captures the essential information required for action classification.

4. **Model Training**:
   - Once features are extracted, a classifier is trained to recognize actions. For this demonstration, a Support Vector Machine (SVM) classifier is used, but other classifiers can be explored based on specific needs.

5. **Evaluation**:
   - The trained model's performance is evaluated using metrics like accuracy, precision, recall, and F1-score. This provides insights into the model's ability to recognize actions accurately.

## Conclusion

This guide offers a foundational approach to action recognition from video frames. The approach uses feature extraction with a pre-trained model and classification with SVM. Depending on the dataset, application, and specific requirements, users might need further refinements and optimizations.

