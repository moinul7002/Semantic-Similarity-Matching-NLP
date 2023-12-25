# Semantic-Similarity-Matching-NLP

Test the similarity between two sentences using online lexical database WordNet. Refer to the original paper of Mihalcea et al. (Corpus-based and Knowledge-based Measures of Text Semantic Similarity), appeared in AAAI 2006. See, (https://www.aaai.org/Papers/AAAI/2006/AAAI06-123.pdf)

1.	From Section 5 of Chapter 2 of NLTK online book, try to reproduce the coding examples and try to use your own examples of wording to identify the synsets, hyponyms, hypernyms, and various semantic similarity between two words of your choice.
2.	Identify the synsets of the word “car” and rank them in the order of their frequency of occurrence
(most common synset first, less common synset at the end). For this purpose, you may use the coding:
car = wn.synsets('car', 'n')[0] print car.lemmas()[0].count()
-> Get the most common synset
-> Get the first lemma
3.	Now consider two sentences T1 and T2, each constituted with a set of tokens. For this purpose, study expression (1) of the aforementioned Mihalcea et al.’s paper above (see below).  You can check with a potential implementation available at https://nlpforhackers.io/wordnet-sentence-similarity/ 
4.	Start with sentences: T1: “Students feel unhappy today about the class today”. T2: ”Many students felt concepts of class test relevant”,  and study the influence of various preprocessing (stopword removal, stemming) on the result of the sentence-to-sentence similarity above.
5.	Implement a program that calculates the sentence-to-sentence similarity as the result of the FuzzyWuzzy score of comparison of string of both sentences, after initial preprocessing and lemmatization using wordnet lemmatizer. Calculate the new similarity score between sentence T1 and T2.
6.	Now consider a new sentence-to-sentence similarity where the similarity score is calculated as the cosine similarity of embedding vectors of the two sentences and where the embedding vector of each sentence is the average of FastText embedding vector of each word constituting the sentence prior to any pre-processing stage. Write a program that implements this similarity metric and compute the sentence-to-sentence similarity of T1 and T2. 
7.	Repeat the above process when using Glove, word2vec embeddings.
8.	Consider the Quora question-answer pair in Question Pairs Dataset (kaggle.com). Write a program that evaluate the sentence-to-sentence similarity using the five methods above (Mihalacea, FuzzyWuzzy and FastText, word2vec, glove) and calculate the score over all pairs, testing pairs. Compare your result with some of results reported in the repository.
