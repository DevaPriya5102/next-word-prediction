# Next Word Prediction using LSTM

## Project Overview
This project develops a next-word prediction model utilizing Natural Language Processing (NLP) techniques to suggest the most likely subsequent word in a given text. Our model leverages Long Short-Term Memory (LSTM) networks, which are adept at maintaining long-term context, outperforming older models such as simple RNNs that struggle with long sequences.

### Team Members
- Poojith Mendem
- Deva Priya Mankena

## Data Preprocessing
We used Shakespeare's "Hamlet" for data collection, which involved tokenizing the text into 4,818 unique tokens. Each line of text was split such that all words except the last formed the independent variables, and the last word was the dependent variable. This method was iteratively applied across the entire text to form subsequence vectors.

## Model Architecture
- **Embedding Layer:** 100-dimensional input.
- **Input Layer:** 150 neurons.
- **Hidden Layers:** Three bi-directional layers with ReLU and Swish activation functions.
- **Output Layer:** 4,818 neurons with a softmax activation function for output classification.
- **Compilation:** Loss function as categorical crossentropy, optimizer as Adam, and accuracy as the metric.

## Improvements and Innovations
The key improvements over previous models include:
- **Vanishing Gradients Mitigation:** The LSTM architecture with its gating mechanisms (input, forget, output gates) addresses the vanishing gradient problem found in simple RNNs.
- **Bidirectional LSTM:** By processing text in both forward and backward directions, it captures richer contextual information, significantly enhancing the prediction accuracy.

## Results
The Bidirectional LSTM model achieved the highest accuracy of 83.47% with the lowest loss rate of 0.56. It substantially outperforms the simple RNN model, which had an accuracy of 43.02% and a loss of 2.50, and a standard LSTM model with an accuracy of 60.81% and a loss of 1.69.

## Future Work
To further enhance the model's performance, future efforts could include:
- Training with more extensive datasets.
- Increasing the number of training epochs.
- Model optimization techniques.
- Utilizing high-end hardware for better computational efficiency.

## Acknowledgments
Special thanks to all contributors and supporters of this project, making this advancement in NLP possible.

