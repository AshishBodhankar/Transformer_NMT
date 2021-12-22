# Understanding the Transformer model from "Attention is all you need" paper

In this project we simultaneously understand and build a smaller distilled version of the Transformer architecture introduced in the "Attention is all you need paper" by Vaswani et. al. This paper was a more advanced step in the use of the attention mechanism being the main basis for a model called Transformer. The most famous current models that are emerging in NLP tasks consist of dozens of transformers or some of their variants, for example, GPT-3 or BERT.

We will describe the components of this model, analyze their operation and build a simple model that we will apply to a small-scale NMT problem (Neural Machine Translation).

# The Dataset
For this exercise we will use pairs of simple sentences, the source in English and target in Spanish, from the Tatoeba project where people contribute adding translations every day. This is the link to some translations in different languages. There you can download the Spanish - English spa_eng.zip file, it contains 124457 pairs of sentences.

We use a list of non breaking prefixes to avoid the tokenizer to split or break words including that prefixes. Inm our example we do not want to remove some the dot for some well-konw words.You can find non breaking prefixes for many languages in the Kaggle website:

https://www.kaggle.com/nltkdata/nonbreaking-prefixes/activity

The text sentences are almost clean, they are simple plain text, so we only need to remove dots that are not a end of sentence symbol and duplicated white spaces.

# Problem description
Machine translation (MT) is the task of automatically converting source text in one language to text in another language. Given a sequence of text in a source language, there is no one single best translation of that text to another language. This is because of the natural ambiguity and flexibility of human language. This makes the challenge of automatic machine translation difficult, perhaps one of the most difficult in artificial intelligence.

From the above we can deduce that NMT is a problem where we process an input sequence to produce an output sequence, that is, a sequence-to-sequence (seq2seq) problem. The encoder-decoder architecture for recurrent neural networks is the standard method.

# Code Content

Transformer-NMT-en-es: This notebook shows how to download and preprocess the text data, create a batch data generator for sequences of data, define and build all the components in a Transformer using the self attention mechanism. We describe the attention mechanism, the encoder and decoder blocks and build the encoder, the decoder and the Transformer and train it for our problem.
