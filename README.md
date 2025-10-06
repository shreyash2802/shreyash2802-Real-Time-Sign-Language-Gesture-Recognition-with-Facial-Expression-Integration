
# Real-Time Sign Language Gesture Recognition with Facial Expression Integration

## Overview
This project presents a real-time multimodal sign language recognition system that integrates gesture recognition and facial emotion detection. The system utilizes deep learning techniques, including CNN-LSTM for gesture recognition and DeepFace for facial emotion analysis, to improve sign language interpretation.

## Features
- **Gesture Recognition**: Uses MobileNetV2 for spatial feature extraction and LSTM for temporal learning.
- **Facial Emotion Detection**: Implements DeepFace to analyze facial expressions for added emotional context.
- **Real-Time Processing**: Operates on live camera input and renders predictions in real time.
- **High Accuracy**: Achieves 92% classification accuracy on the Small WLASL dataset.
- **Improved Context Understanding**: Resolves ambiguities in similar gestures by integrating facial expressions.

## Methodology
1. **Data Preprocessing**:
   - Uses the Small WLASL dataset with 50 sign language gestures.
   - Frames are resized to 224×224 and normalized.
   - Videos are padded to 30 frames for uniform sequence length.
2. **Model Architecture**:
   - MobileNetV2 extracts spatial features from video frames.
   - LSTM models temporal dependencies for gesture classification.
   - DeepFace processes facial expressions and classifies emotions.
   - Outputs from both models are fused for final classification.
3. **Implementation**:
   - Developed using TensorFlow and OpenCV.
   - Trained on Google Colab with a GPU (50GB VRAM).
   - Uses the Adam optimizer with a learning rate of 0.001.
4. **Real-Time Execution**:
   - Captures live webcam feed.
   - Preprocesses frames and passes them through the two models.
   - Displays recognized gestures and emotions in real time.

## Performance Metrics
| Metric     | Value (%) |
|------------|----------|
| Accuracy   | 92.0     |
| Precision  | 89.8     |
| Recall     | 90.2     |

## Comparison with Existing Methods
| Method                | Model Used                 | Facial Analysis | Real-Time |
|-----------------------|---------------------------|----------------|-----------|
| Kumari et al.        | CNN-LSTM + Self Attention  | No             | No        |
| Chung et al.         | PoseNet + GCN             | Partial        | No        |
| Huang et al.         | 3D-CNN                     | No             | No        |
| **Proposed Method**  | MobileNetV2 + LSTM + DeepFace | **Yes**    | **Yes**   |

## Installation
1. Clone the repository:
   ```sh
   git clone https://github.com/your-repo/sign-language-recognition.git
   cd sign-language-recognition
   ```
2. Install dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the real-time recognition script:
   ```sh
   python main.py
   ```

## Future Improvements
- Expand dataset diversity using multi-signer datasets.
- Optimize model with lightweight transformer-based architectures.
- Deploy on mobile devices for accessible sign language translation.

## Contributors
- Sagar Shegunashi
- Vishwanath Hubballi
- Shreyas Rawate
- K. Koushik Kumar Reddy



