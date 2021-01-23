# Portuguese to English Translation with Encoder-Decoder Model

This project uses a dataset called [Europarl](https://www.statmt.org/europarl/), a collection of parallel sentence translations in many languages from European Parliament proceedings. It is described in the paper [Europarl: A Parallel Corpus for Statistical Machine Translation, Philipp Koehn, MT Summit 2005](http://www.iccs.inf.ed.ac.uk/~pkoehn/publications/europarl-mtsummit05.pdf).

I use the Portuguese/English translations to train an encoder-decoder model to generate English translations of Portuguese sentences. 

## Features:
- an encoder-decoder model built from only three basic PyTorch layers: Linear, Embedding, and LSTM
- an implementation of "teacher forcing" that only uses true labels as inputs at each sequence step with a given probability each epoch
- a model that handles training and inference with the same method, even though the functionality is different (inference doesn't use any true labels)
- a training method that can increase the difficulty each epoch by using fewer of the true labels
- my own implementations of tokenization, numericalization, and batching

