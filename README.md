# Sentence_Embeddings
Word embeddings and sentence embeddings are the bread and butter of LLMs. They are the basic building block of most language models.

## What is a Word Embedding?
Firstly, Word embeddings are a technique used in natural language processing (NLP) to represent words as numerical vectors in a continuous space. These vectors capture semantic relationships between words, allowing computers to understand and process language more effectively.

Imagine you have a dictionary-like representation where each word is associated with a unique vector of numbers. In this vector space, words with similar meanings or contexts are positioned closer to each other. Word embeddings capture the inherent semantic relationships and contextual information of words based on their usage patterns in large text corpora.

For instance, consider the words "king," "queen," "man," and "woman." In a good word embedding space, the vectors for "king" and "queen" would be closer to each other compared to the vectors for "man" and "woman." The vector direction from "king" to "queen" should be similar to the vector direction from "man" to "woman." This reflects the understanding that "king" and "queen" are related in the same way as "man" and "woman," but with different gender and roles.

Mathematically, these word vectors are real-valued vectors with dimensions (often ranging from 100 to 300 dimensions), where each dimension encodes a specific aspect of the word's meaning or context. Word embeddings are typically trained using machine learning models like Word2Vec, GloVe, or FastText on large text corpora. Once trained, these embeddings can be used as features for various NLP tasks like text classification, sentiment analysis, machine translation, and more.

