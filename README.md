# Character-Level Seq2Seq Text Translation

This repository contains a Jupyter Notebook implementing a character-level Sequence-to-Sequence (Seq2Seq) model using Keras and TensorFlow. The model is trained to translate standard English text into a simplified "robotic" version (e.g., replacing specific letters with numbers).

## Features
* **Character-Level Tokenization:** Maps unique characters from the input and target texts into index dictionaries.
* **One-Hot Encoding:** Vectorizes text data into multi-dimensional NumPy arrays for training.
* **Encoder-Decoder LSTM Architecture:** Utilizes an Encoder LSTM to capture context and a Decoder LSTM to generate the translated sequence.
* **Inference Pipeline:** Features a standalone inference encoder and decoder loop to predict text iteratively.

## Prerequisites & Dependencies
The project requires Python 3 and the following Python libraries:
* `numpy`
* `tensorflow` (which includes `keras`)

## How It Works

* **Data Preprocessing:** Parses basic input phrases (e.g., `"hello"`, `"how are you"`) and target robotic phrases (e.g., `"h3ll0"`, `"h0w 4r3 y0u"`)[cite: 1].
* **Model Training:** Builds and trains the Seq2Seq network using the `rmsprop` optimizer and `categorical_crossentropy` loss over 5 epochs[cite: 1].
* **Sequence Decoding:** Uses a dedicated `decode_sequence` function to predict target characters step-by-step using the trained internal states[cite: 1].

  
To install the required packages, run:
```bash
pip install numpy tensorflow
