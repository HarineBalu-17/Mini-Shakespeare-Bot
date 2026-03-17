Mini-Shakespeare Bot 🎭
This project features a character-level text generation model built using a Long Short-Term Memory (LSTM) network. It is trained on Shakespearean dialogue to predict and generate text in a similar stylistic vein, deployed via an interactive Gradio web interface.

Features
LSTM Neural Network: Utilizes a Sequential model with a 128-unit LSTM layer to capture sequential dependencies in text.
Character-Level Prediction: Maps unique characters to indices to predict the next character in a sequence.
Temperature-Based Sampling: Implements a temperature parameter (default 0.6) to balance predictable vs. creative text generation.
Interactive Web UI: Includes a Gradio interface where users can input a seed phrase and receive generated Shakespearean-style prose.

Tech Stack
Deep Learning Framework: TensorFlow / Keras
Web Interface: Gradio
Data Manipulation: Pandas, NumPy
Environment: Python 3 (Optimized for Google Colab)

How It Works
Preprocessing: The model processes 8,000 lines from the Shakespeare dataset, converting them to lowercase and creating a character mapping.
Vectorization: Text is broken into sequences of 40 characters (maxlen) with a step of 3, then converted into one-hot encoded boolean arrays.
Architecture:LSTM Layer: 128 units to process the $40 \times \text{total\_chars}$ input shape.
             Dense Layer: A Softmax output layer that matches the number of unique characters in the vocabulary.
Training: The model is compiled with the adam optimizer and categorical_crossentropy loss function, trained for 5 epochs with a batch size of 512.

Installation & Usage
Clone the repository:

Bash
git clone https://github.com/your-username/shakespeare-lstm-generator.git
Install dependencies:

Bash
pip install pandas numpy tensorflow gradio
Run the Notebook:
Open DL_8.ipynb in Google Colab or a local Jupyter environment and run all cells to launch the Gradio public URL.

Training Summary
Epochs: 5

Final Training Loss: 2.1745

Processing Time: ~72–82 seconds per epoch

Note: This version is a "Mini" bot trained on a limited subset (8,000 lines) for speed. For higher-quality, more coherent prose, increase the dataset size and the number of training epochs.
<img width="1495" height="545" alt="image" src="https://github.com/user-attachments/assets/df342346-bac8-4047-bef8-d620efb00c1c" />

