# Deep Learning Language Modelling

A deep learning language modelling project exploring the progression from recurrent neural networks to Transformer-based architectures on *Alice's Adventures in Wonderland*.

## Project Overview

This project compares several approaches to language modelling, including character-level and word-level GRU models, pre-trained word embeddings, a decoder-only Transformer trained from scratch, and fine-tuning of a pre-trained DistilGPT-2 model.

The goal was to understand how model architecture and pre-training affect text generation quality, training efficiency, and perplexity.

## Models Implemented

* Character-level GRU language model
* Word-level GRU language model
* Word-level GRU with pre-trained GloVe embeddings
* Decoder-only causal Transformer
* Fine-tuned DistilGPT-2

## Tools & Technologies

* Python
* TensorFlow / Keras
* PyTorch
* Hugging Face Transformers
* GloVe embeddings

## Methodology

The project began with a character-level GRU model using token sequences generated from the source text. The pipeline was then adapted to word-level modelling to compare different tokenisation granularities.

Pre-trained GloVe embeddings were introduced to evaluate the benefit of transferring semantic information from large external corpora.

A decoder-only Transformer was subsequently implemented from scratch and compared with recurrent architectures.

Finally, DistilGPT-2 was fine-tuned on the same corpus using a custom PyTorch training loop to examine the effect of transfer learning from a pre-trained language model.

## Key Results

* The decoder-only Transformer achieved a final training loss of **0.42** after 50 epochs.
* Fine-tuning DistilGPT-2 reduced perplexity from **27.6 to 13.3** within 3 epochs, an improvement of approximately **52%**.
* Introducing pre-trained GloVe embeddings reduced the initial training loss of the word-level GRU by approximately **40%** compared with training embeddings from scratch.


## Dataset

The training corpus was *Alice's Adventures in Wonderland* by Lewis Carroll.

