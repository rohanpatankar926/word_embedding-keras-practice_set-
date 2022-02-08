# word_embedding-keras

# Word Embedding
-->A word embedding is a class of approaches for representing words and documents using a dense vector representation.

-->It is an improvement over more the traditional bag-of-word model encoding schemes where large sparse vectors were used to represent each word or to score each word within a vector to represent an entire vocabulary. These representations were sparse because the vocabularies were vast and a given word or document would be represented by a large vector comprised mostly of zero values.

-->Instead, in an embedding, words are represented by dense vectors where a vector represents the projection of the word into a continuous vector space.

-->The position of a word within the vector space is learned from text and is based on the words that surround the word when it is used.

-->The position of a word in the learned vector space is referred to as its embedding.

-->Two popular examples of methods of learning word embeddings from text include:

-->Word2Vec.
-->GloVe.

-->In addition to these carefully designed methods, a word embedding can be learned as part of a deep learning model. This can be a slower approach, but tailors the model to a specific training dataset.
