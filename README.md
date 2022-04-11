# Text-generation

# Angelos Nikolas 

The objective is to train a word-level language model using the text from the book “Poirot
Investigates” by Agatha Christie (https://www.gutenberg.org/ebooks/61262).

The dataset can be downloaded here in plain text format:
https://www.gutenberg.org/files/61262/61262-0.txt

### Code Overview
Firstly, the raw text was loaded from the link, some exploration occurred to define errors within the text. It was deemed necessary to clean the file by removing special characters and other various elements. Then a corpus containing all the words was created and from this corpus a vocabulary of unique words was created. From the dictionary list that was created, sentences in new list were assigned. Sentences of 41 words were stored, the 41st word is specified as the target variable. Using the tokenizer library each word was transformed into a numerical value and converted from one dimensional list to multidimensional container of items of the same type and size. The Long Short Term Memory (LSTM) is used for the text generation, 2 LTSM layers were utilized having 64 units in total, in addition 1 dense layer having 128 nodes. As for the hyperparameters Adam optimizer was used the activation function Rectified Linear Unit (ReLU) was used due to low computation requirements and versatile nature. A batch size of 64 was used as suggested for this kind of operation.
Example text input: “This is 50-word sentence to test some text generation from the writings of Agatha Christie how exciting it is!”
Generated output: “gagged and reported me no i said let us start to you for damages costs and expenses including legal fees that arise directly or indirectly from Liverpool were suspicious revoir a solitaire Italian on you and done now here the man prepared to shut the door I saw no mouse”
