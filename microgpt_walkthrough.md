# microgpt.py: Annotated Walkthrough

This document is designed to help students understand the structure and function of the `microgpt.py` code. The script demonstrates how to train and run inference for a GPT-like model in pure Python, with minimal dependencies. Below, each major component is explained in plain language.

---

## 1. Data Preparation
- **Dataset Loading:**
  - If `input.txt` does not exist, it downloads a list of names from the internet.
  - Reads the file into a list of documents (`docs`), shuffles them for randomness.
- **Tokenizer:**
  - Finds all unique characters in the dataset.
  - Assigns each character a unique token ID.
  - Adds a special Beginning of Sequence (BOS) token.

## 2. Autograd Engine
- **`Value` Class:**
  - Represents a scalar value in the computation graph.
  - Supports basic math operations and tracks how each value was computed.
  - Implements backpropagation to compute gradients for learning.

## 3. Model Parameters
- **Parameter Initialization:**
  - Sets up the neural network's weights (parameters) for embeddings, attention, and MLP layers.
  - Uses random values for initialization.

## 4. Model Architecture (GPT)
- **`gpt()` Function:**
  - Defines a single-layer transformer (like GPT-2, but simpler).
  - Steps:
    1. Embeds tokens and positions.
    2. Applies layer normalization (RMSNorm).
    3. Runs multi-head self-attention.
    4. Runs a feedforward (MLP) block.
    5. Outputs logits (predictions for next token).
- **Supporting Functions:**
  - `linear()`: Matrix multiplication for neural network layers.
  - `softmax()`: Converts logits to probabilities.
  - `rmsnorm()`: Normalizes vectors for stability.

## 5. Training Loop
- **Adam Optimizer:**
  - Implements the Adam optimization algorithm for updating parameters.
- **Training Steps:**
  - For each step:
    1. Tokenizes a document.
    2. Runs the model to compute the loss (how wrong the prediction is).
    3. Computes gradients via backpropagation.
    4. Updates parameters using Adam.
    5. Prints the current loss.

## 6. Inference (Text Generation)
- **Sampling:**
  - After training, generates new names by sampling from the model.
  - Uses the learned parameters to predict one character at a time.
  - Stops when the BOS token is generated or the max length is reached.

---

## Key Takeaways
- This script is a minimal, readable implementation of a GPT-like model.
- It covers data loading, tokenization, model definition, training, and inference.
- All neural network and autograd logic is implemented from scratch for educational clarity.

---

Students should walk through each section, relate the code to these explanations, and discuss how each part contributes to the overall process of training and generating text with a neural network.
