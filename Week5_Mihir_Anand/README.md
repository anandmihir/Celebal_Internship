# Text Generation Using RNN, LSTM, and GRU

## Overview

This project implements a Deep Learning-based text generation system using three recurrent neural network architectures:

* Vanilla SimpleRNN
* Long Short-Term Memory (LSTM)
* Gated Recurrent Unit (GRU)

The objective is to train these models on a text corpus so they can learn word sequences, grammatical patterns, and contextual dependencies to generate new text from a given seed phrase.

## Project Workflow

1. Load and preprocess the input text corpus.
2. Tokenize the text and convert words into integer sequences.
3. Create progressive n-gram sequences.
4. Apply padding to ensure equal sequence lengths.
5. Separate the sequences into input features (`X`) and target labels (`y`).
6. Build SimpleRNN, LSTM, and GRU models.
7. Train all models using the Adam optimizer.
8. Compare model performance using training loss curves.
9. Generate text using a common seed phrase.
10. Use `np.argmax()` to select the next predicted word.

## Models Implemented

### Vanilla SimpleRNN

SimpleRNN processes sequential information using a recurrent hidden state. It serves as the baseline model for comparing recurrent architectures.

### LSTM

LSTM uses memory cells and gating mechanisms to capture long-term dependencies and reduce the vanishing gradient problem.

### GRU

GRU is a simplified gated recurrent architecture that uses fewer gates than LSTM while maintaining the ability to learn long-term dependencies.

## Student Customization Tasks

The following modifications were implemented:

* Replaced the original boilerplate corpus with a custom Data Science-related text corpus.
* Increased the embedding dimension.
* Expanded model training from 100 to 200 epochs.
* Increased hidden layer units from 64 to 128.
* Increased generated output length to 10 words.

## Technologies Used

* Python
* TensorFlow
* Keras
* NumPy
* Matplotlib
* Google Colab / Jupyter Notebook

## Model Evaluation

The training loss of SimpleRNN, LSTM, and GRU is plotted on a single line graph. This allows comparison of the cross-entropy loss reduction and training stabilization of all three models.

## Text Generation

A common seed phrase is provided to all three trained models. The models predict the next word using the probability distribution produced by the output layer.

The next word is selected using:

`np.argmax()`

The predicted word is repeatedly added to the input sequence to generate a complete text sequence.

## Output

The project produces:

* Training loss curves for SimpleRNN, LSTM, and GRU.
* Generated text from the SimpleRNN model.
* Generated text from the LSTM model.
* Generated text from the GRU model.
* A comparison of the learning behavior of all three architectures.

## Conclusion

This project demonstrates how recurrent neural network architectures can be used for text generation. SimpleRNN provides a basic approach to sequential learning, while LSTM and GRU use gating mechanisms to better capture contextual and long-term dependencies. Comparing the three models provides practical insight into their training behavior and text-generation capabilities.
