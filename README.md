# Image-Captioning

Image Captioning System with Transfer Learning and RNN
This project implements an Image Captioning System that generates descriptive captions for images using Transfer Learning for feature extraction and a Recurrent Neural Network (RNN) for caption generation. It is built on the Flickr8k dataset and aims to achieve over 85% accuracy on validation data. The system can also be extended to real-time captioning using live camera feeds.

📜 Features
Image Feature Extraction:
Utilized pre-trained CNN model InceptionV3 to extract high-level features from images.

Caption Generation:
Employs a simple RNN as a decoder to generate captions sequentially.
Real-Time Captioning:
Integrates with OpenCV to describe live camera feeds in natural language.
Metrics and Evaluation:
Evaluates caption quality using BLEU score or CIDEr to measure relevance against ground-truth captions.

🛠️ How It Works
1. Feature Extraction
Preprocesses images to fit the input requirements of the pre-trained CNN model.
Extracts and saves fixed-length feature vectors for each image as numpy arrays for efficient reuse.
2. Caption Preprocessing
Cleans and tokenizes captions by:
Converting text to lowercase.
Removing special characters.
Tokenizing words.
Builds a vocabulary by filtering frequently occurring words.
Converts captions into sequences of integers with <start> and <end> tokens.
3. Model Architecture
Transfer Learning:
Uses a pre-trained CNN to extract image features.
Caption Decoder:
Embedding layer to encode words into dense representations.
RNN for sequence modeling and word generation.
Dense layer to predict the next word in the sequence.
Training:
Optimizes using categorical cross-entropy loss and the Adam optimizer.
4. Real-Time Captioning
Captures live images using OpenCV.
Passes images through the trained model to generate captions with minimal latency.

📊 Performance
Training Accuracy: Achieves over 85% on validation data.
Evaluation Metrics: Measures BLEU and CIDEr scores for caption relevance and coherence.
Generalization: Incorporates regularization techniques like dropout to prevent overfitting.
