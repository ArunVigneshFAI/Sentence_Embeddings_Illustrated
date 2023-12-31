# Sentence_Embeddings
Word embeddings and sentence embeddings are the bread and butter of LLMs. They are the basic building blocks of most language models.

## What is a Word Embedding?
Firstly, Word embeddings are a technique used in natural language processing (NLP) to represent words as numerical vectors in a continuous space. These vectors capture semantic relationships between words, allowing computers to understand and process language more effectively.

Imagine you have a dictionary-like representation where each word is associated with a unique vector of numbers. In this vector space, words with similar meanings or contexts are positioned closer to each other. Word embeddings capture the inherent semantic relationships and contextual information of words based on their usage patterns in large text corpora.

For instance, consider the words "king," "queen," "man," and "woman." In a good word embedding space, the vectors for "king" and "queen" would be closer to each other compared to the vectors for "man" and "woman." The vector direction from "king" to "queen" should be similar to the vector direction from "man" to "woman." This reflects the understanding that "king" and "queen" are related in the same way as "man" and "woman," but with different gender and roles.

Mathematically, these word vectors are real-valued vectors with dimensions (often ranging from 100 to 300 dimensions), where each dimension encodes a specific aspect of the word's meaning or context. Word embeddings are typically trained using machine learning models like Word2Vec, GloVe, or FastText on large text corpora. Once trained, these embeddings can be used as features for various NLP tasks like text classification, sentiment analysis, machine translation, and more.

## What is a Sentence Embedding?
Word embeddings indeed prove highly valuable, yet human language's complexity extends beyond mere word combinations. Language encompasses structure, sentences, and more intricate nuances. Representing sentences poses a challenge, and a straightforward approach might involve summing the scores of individual words. For instance, if word embeddings allocate scores like:

"No": [1, 0, 0, 0]
"I": [0, 2, 0, 0]
"Am": [-1, 0, 1, 0]
"Good": [0, 0, 1, 3]

The sentence "No, I am good!" would equate to the vector [0, 2, 2, 3]. However, the sentence "I am no good" would also yield the vector [0, 2, 2, 3]. This approach doesn't distinguish between these two quite distinct sentences, despite their opposing meanings.

To address this limitation, sentence embeddings emerge as a solution. Analogous to word embeddings, sentence embeddings associate each sentence with a coherent numerical vector. Coherence ensures that similar sentences share similar vectors, diverse sentences possess distinct vectors, and crucially, each vector component signifies a specific aspect of the sentence, whether overt or subtle.

![image](https://github.com/ArunVigneshFAI/Sentence_Embeddings_Illustrated/assets/141916176/18886f91-5b9e-4e48-a7fd-e65941eee4f9)

The LLM sentence embedding achieves precisely this objective. Leveraging advanced algorithms such as transformers and attention mechanisms, this embedding transforms each sentence into a vector composed of a lot of numerical values - let's say 4096 numerical values. This embedding approach has demonstrated remarkable performance.

For illustrative purposes, a heatmap of the initial 10 entries of various sentences is provided below. Due to space limitations, the complete set of 4096 entries is truncated here.

![image](https://github.com/ArunVigneshFAI/Sentence_Embeddings_Illustrated/assets/141916176/d6719f17-8428-4601-afaa-0d9577b59ae2)

It's noteworthy that the presented sentences exhibit significant similarity. Notably, the three highlighted sentences convey almost identical meanings. Upon examining their corresponding vectors, it becomes evident that these vectors are also remarkably similar. This outcome aligns precisely with the intended function of an embedding.

## How to Use These Embeddings?
Having gained an appreciation for the utility of these embeddings, the exploration of practical applications begins. A small illustrative example is provided below, involving the following phrases:

- I like my dog
- I love my dog
- I adore my dog
- Hello, how are you?
- Hey, how's it going?
- Hi, what's up?
- I love watching soccer
- I enjoyed watching the world cup
- I like watching soccer matches

The resultant output manifests as vectors, each comprising 4096 entries for every sentence. While visualizing these high-dimensional vectors might prove challenging, a method exists to condense them into two entries per sentence for convenient visualization. The ensuing plot captures this visualization.

![image](https://github.com/ArunVigneshFAI/Sentence_Embeddings_Illustrated/assets/141916176/e4d4d54a-b3ab-4d45-b6af-433a38b9753a)

An observed phenomenon is that the embedding adeptly encapsulates the core essence of the sentences, leading to the emergence of three distinct sentence clusters. Positioned in the upper-left quadrant are sentences of greetings, while the middle cluster pertains to discussions about individuals' dogs. In the lower-right corner, sentences relating to soccer are concentrated. An intriguing observation is that even sentences like "Hey, what's up?" and "Hello, how are you?" share no common words, yet the model discerns their shared meaning, illustrating the embedding's ability to capture nuanced semantic relationships.

## Conclusion
Word and sentence embeddings stand as foundational elements within the realm of LLMs. Serving as fundamental constructs of most language models, they facilitate the conversion of human language (words) into a computational format (numbers). This translation process adeptly captures the intricate web of word relationships, semantic nuances, and linguistic intricacies, translating them into numerical representations that can be manipulated through mathematical operations.

Expanding on this notion, sentence embeddings can be broadened into language embeddings, where the numerical values associated with each sentence remain language-agnostic. These models prove highly advantageous for tasks such as translation, as well as for the search and comprehension of text across different languages.
