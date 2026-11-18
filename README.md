# BERT Visualizer

A beginner-friendly project to understand how **BERT (Bidirectional Encoder Representations from Transformers)** processes text using the Hugging Face Transformers library.

## Overview

This project explores the basic working of the BERT model through Python and Google Colab. It demonstrates how text is converted into tokens, how tokens are converted into numerical input, and how BERT generates contextual representations.

The goal is to understand the internal flow of BERT step by step rather than simply using it as a black-box model.

## Features

- Load the pretrained `bert-base-uncased` model.
- Tokenize input text using the BERT tokenizer.
- Convert text into input IDs, attention masks, and token type IDs.
- Pass tokenized inputs through the BERT encoder.
- Inspect the shape of the final hidden-state output.
- Understand batch size, sequence length, and hidden dimensions.

## Technologies Used

- Python
- Google Colab
- PyTorch
- Hugging Face Transformers
- SentencePiece

## Installation

Install the required libraries:

```bash
pip install transformers sentencepiece
```

PyTorch is also required. Google Colab generally provides it by default.

## How to Run

1. Open the notebook in Google Colab.
2. Install the required dependencies.
3. Load the pretrained BERT tokenizer and model.
4. Provide a sample sentence as input.
5. Tokenize the sentence and inspect the generated inputs.
6. Pass the inputs through BERT.
7. Examine the shape of the final hidden-state output.

## Understanding the Output

BERT Base produces a hidden representation of size **768 for each input token**.

For example, if one sentence contains 6 tokens, the final hidden-state tensor has the shape:

```text
[1, 6, 768]
```

Where:

- `1` represents the batch size (one sentence).
- `6` represents the number of tokens.
- `768` represents the hidden dimension or number of features for each token.

## Learning Objectives

Through this project, I aim to understand:

- How tokenization works in BERT.
- How input text is represented numerically.
- How BERT processes tokenized input.
- What contextual embeddings and hidden states represent.
- How batch size, sequence length, and hidden dimensions relate to one another.

## Future Improvements

- Visualize BERT's encoder architecture.
- Explore token embeddings and positional embeddings.
- Understand self-attention and multi-head attention.
- Visualize attention weights between tokens.
- Experiment with sentence representations and pooling.

## References

- [Hugging Face Transformers Documentation](https://huggingface.co/docs/transformers)
- [BERT Paper – Devlin et al. (2018)](https://arxiv.org/abs/1810.04805)
- [Google Colab](https://colab.research.google.com/)

