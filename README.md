# nlp-module1-assignment
The goal for this assignment id to processes text from Shakespeare's works to analyze n-grams and compute probabilities of word sequences. The notebook utilizes Natural Language Processing (NLP) techniques to preprocess text, extract n-grams, and determine the likelihood of words following a given n-gram.

## Tasks

### Task 1: Data Preparaion
1. **Read Shakespeare's Works:**
- Load a text file containing Shakespeare's works.
- Preprocess the text by converting it to lowercase, removing punctuation, and splitting it into tokens.
- Create a list of bigrams from the preprocessed text.

2. **Dictionary of Bigram Counts:**
- Write the code that fills the from_bigram_to_next_token_counts dictionary, where each key is a bigram (tuple of two tokens) and the value is a dictionary of counts of tokens that follow the bigram.
- Example: 
```
from_bigram_to_next_token_counts[('to', 'be')] = {'or': 10, 'not': 5}
```

### Task 2: Probability Distribution
1. **Calculate Probabilities**
- Write the code that fills the from_bigram_to_next_token_probs dictionary, where each key is a bigram and the value is a dictionary of probabilities of tokens that follow the bigram.
- Use the counts from from_bigram_to_next_token_counts to calculate the probabilities.
- Example: 
```
from_bigram_to_next_token_probs[('to', 'be')] = {'or': 0.67, 'not': 0.33}
```

### Task 3: Sampling the Next Token
1. **Implement a Sampling Function**
- Implement the sample_next_token function, which should return the next token sampled based on the probability distribution from from_bigram_to_next_token_probs.
- Ensure the sampling is done using a weighted random choice.

### Task 4: Generating Text
1. **Generate Text**
- Implement the generate_text_from_bigram function, which generates text by starting with an initial bigram and sampling the next token iteratively.
- The function should return a string of generated text with a specified number of words.
- Example: generate_text_from_bigram(('to', 'be'), 50) might return "to be or not to be that is the question ..."

### Task 5: Exploration of Different N-grams
1. **Experiment with Trigrams and Quadgrams:**
- Extend the model to work with trigrams (3-grams) and quadgrams (4-grams).
- Implement similar functions for these n-grams: from_trigram_to_next_token_counts, from_trigram_to_next_token_probs, from_quadgram_to_next_token_counts, and from_quadgram_to_next_token_probs.
- Analyze the differences in text generation quality between bigrams, trigrams, and quadgrams.

### Task 6: Human Evaluation
1. Human Evaluation:
- Design a survey to collect feedback from human participants on the quality of the generated text.
- Analyze the feedback to gain insights into how well your model imitates the style of Shakespeare.

At the time of submiting this assignment, 9 people rated one of my generated texts. The ratings fo from 1 to 5, first based on similarity to Shakespeare's language, and then on coherence:
![image](https://github.com/user-attachments/assets/9c15570b-c8b9-4e0b-9788-83496a8f6be1)
![image](https://github.com/user-attachments/assets/a381eb16-eeda-4cb5-b125-228e2ee04a7f)

## Tests
On the bottom of the notebook, there are tests for each of the functions used to fulfill the tasks of this assignment.

## Requirements
To run this notebook, install the required dependencies:
```bash
pip install nltk random unittest
```

## Running the Notebook
1. Open Jupyter Notebook.
2. Load and execute the notebook step by step to process the text and compute bigram probabilities.

## Expected Output
- Preprocessed tokenized text from Shakespeare’s works.
- A dictionary mapping n-grams to their respective word frequencies.
- A probability distribution for each bigram based on observed counts.
- A generated text based on n-gram probabilities.

## References:
- [NLTK](https://www.nltk.org/)
- [Gutenberg Corpus](https://www.nltk.org/book/ch02.html)
- [Shakespeare's Works](https://www.gutenberg.org/ebooks/100)
- [Random Sampling](https://docs.python.org/3/library/random.html)
- [Unittest](https://docs.python.org/3/library/unittest.html)

