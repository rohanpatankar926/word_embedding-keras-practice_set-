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

# keras Embedding Layer
-->Keras offers an Embedding layer that can be used for neural networks on text data.

-->It requires that the input data be integer encoded, so that each word is represented by a unique integer. This data preparation step can be performed using the Tokenizer API also provided with Keras.

-->The Embedding layer is initialized with random weights and will learn an embedding for all of the words in the training dataset.

-->It is a flexible layer that can be used in a variety of ways, such as:

-->It can be used alone to learn a word embedding that can be saved and used in another model later.
-->It can be used as part of a deep learning model where the embedding is learned along with the model itself.
-->It can be used to load a pre-trained word embedding model, a type of transfer learning.
-->The Embedding layer is defined as the first hidden layer of a network. It must specify 3 arguments:

-->It must specify 3 arguments:

-->**input_dim**: This is the size of the vocabulary in the text data. For example, if your data is integer encoded to values between 0-10, then the size of the vocabulary would be 11 words.</br>
-->**output_dim**: This is the size of the vector space in which words will be embedded. It defines the size of the output vectors from this layer for each word. For example, it could be 32 or 100 or even larger. Test different values for your problem.</br>
-->**input_length**: This is the length of input sequences, as you would define for any input layer of a Keras model. For example, if all of your input documents are comprised of 1000 words, this would be 1000.</br>
-->For example, below we define an Embedding layer with a vocabulary of 200 (e.g. integer encoded words from 0 to 199, inclusive), a vector space of 32 dimensions in which words -->will be embedded, and input documents that have 50 words each.</br>

-->*e = Embedding(200, 32, input_length=50)*</br>
-->The Embedding layer has weights that are learned. If you save your model to file, this will include weights for the Embedding layer.,/br>

-->The output of the Embedding layer is a 2D vector with one embedding for each word in the input sequence of words (input document).</br>

-->If you wish to connect a Dense layer directly to an Embedding layer, you must first flatten the 2D output matrix to a 1D vector using the Flatten layer.</br>

# References:
[Blog](https://machinelearningmastery.com/use-word-embedding-layers-deep-learning-keras/)</br>
[Video](https://www.youtube.com/watch?v=pO_6Jk0QtKw&list=PLZoTAELRMXVPGU70ZGsckrMdr0FteeRUi&index=42)
