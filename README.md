# 22MCB0038-text-and-speech-analytics-lab-chatbot

Here are the importannt steps done in the project

Import the necessary libraries:

nltk: The Natural Language Toolkit library for text processing and analysis.
stopwords: A list of common words that can be ignored during text analysis.
word_tokenize: A function for tokenizing sentences into words.

Download NLTK resources:
The code downloads the required NLTK resources by using the nltk.download() function. It downloads the punkt tokenizer and the stopwords corpus.

Define the chatbot's responses:
The qa_pairs dictionary stores a set of questions and their corresponding answers. You can modify this dictionary to add or remove questions and answers as per your requirements.

Preprocess user input:

The preprocess_input() function takes a text input and performs the following preprocessing steps:
Converts the input to lowercase to ensure case insensitivity.
Tokenizes the input into individual words using word_tokenize().
Removes stopwords (common words like "is," "are," "the," etc.) from the tokenized words.

Calculate similarity between input and response:

The calculate_similarity() function takes two sets of tokens (input tokens and response tokens) and calculates their similarity using the Jaccard similarity coefficient.
It finds the common tokens between the two sets and divides it by the total number of tokens in the input set to get a similarity score.

Get the most appropriate response:

The get_response() function takes the user's input and finds the most appropriate response from the qa_pairs dictionary.
It iterates over each question-answer pair, calculates the similarity between the input and the question, and keeps track of the response with the highest similarity score.

Chatbot interaction loop:

The code enters a while loop that allows the chatbot to interact with the user.
It takes user input using the input() function and assigns it to the user_input variable.
If the user enters "exit," the loop breaks and the program terminates.
Otherwise, the code calls the get_response() function with the user's input and assigns the response to the response variable.
The response is then printed to the console using print().
