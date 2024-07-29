# Word-and-Character-Text-Generation-Models

## Dataset
The dataset is generated about NLP, image processing, and AI.

## Preprocessing
- Removed numbers, non-English words, punctuations, and any weird words
- Kept white spaces and stop words

## Word-based Model
- Used a tokenizer to give words IDs
- Made sentences as lists of word IDs and the labels of sentences as the word right after each sentence
- Padded sentences to ensure uniform length
- Got word embeddings of the words
- Got one-hot encodings of the labels
- Made the RNN model with an embedding layer, 2 SimpleRNN layers, and a Dense layer
- Generated words by getting the IDs of the words of the input sentences and using the model to predict the next word

**Output**: 
Natural language processing (NLP) is an interdisciplinary subfield of computer science and information retrieval primarily concerned with giving computers the ability to support and manipulate human language.

## Character-based Model
- Made lists of characters with a number of steps between each list and the labels as the character after each list
- Converted lists and labels to integers (IDs)
- Got one-hot encodings of the labels
- Got embeddings of the characters
- Made the RNN model with an embedding layer, 2 SimpleRNN layers, and a Dense layer
- Generated characters by getting IDs of characters of the input sentence and using the model to predict the next character

**Output**: 
Language processing is an interdisciplinary subfield of computer science and information that their artificial intelligence.

## Conclusion
- Character-based model is slower since the list of characters is long, but it can capture spelling errors.
- Word-based model is faster in training but cannot capture spelling errors.
