# NLP
 News Classification Using Naive Bayes Algorithm  
 	NAİVE BAYES
Naive Bayes algorithm is based on Bayes' theorem as shown below and is particularly effective in handling text classification tasks. It assumes that the presence of a particular feature in a class is independent of the presence of other features. Despite this "naive" assumption, Naive Bayes often performs well in practice and is computationally efficient.

P(A\B)=(P(B\A)*P(A))/P(B) 
                                                                                                                                                  (1)
	P(A|B) = probability of A if B occurs
	P(B|A) = probability of B if A occurs
	P(A) = probability of A
	P(B) = probability of A

In the Scikit-learn library, there are different variations of the Naive Bayes classification algorithm:
BernoulliNB: It is used for binary data sets where features are encoded as 1 if they occur in a specific class, and 0 otherwise.
MultinomialNB: It is used for multi-class classification and counts the frequency of features across classes.
GaussianNB: It is a classification algorithm based on the assumption of normally(Gaussian) distribution, where mean and variance of features are calculated for each class.

Considering its features, the use of GaussianNB was deemed appropriate in this project.


	GAUSSİAN
GaussianNB is a variant of the Naive Bayes algorithm that assumes the likelihood of features to follow a Gaussian distribution. In the context of text classification, each feature can represent a word or a term, and the algorithm models the probability distribution of each class based on the mean and variance of the features in that class. Another advantage of GaussianNB is that it is computationally fast and has low memory requirements. In addition, its ability to give good results even in small data sets has been one of the reasons for preference.
# Create the Gaussian Naive Bayes classifier
nb = GaussianNB()

	ALGORITHM IMPLEMENTATION

The implementation of GaussianNB involves several steps:
Data Preprocessing: The text data from the news articles needs to be preprocessed before feeding it into the algorithm. This typically involves steps such as tokenization, removing stopwords, and converting the text into numerical representations suitable for machine learning algorithms.
	Lemmatization: It is a process of make the same words in their stem. For example run, ran, running are different in terms of Python. We lemmatiza the word to get run.
	Stop words: The words that are not important in terms of the context.
	Tokenization: The process of extracting words in a sentence by spaces and punctuations. In this project we'll use nltk's word_tokenize.
	Bag Of Words: BoW is the representation of text data in a numerical way that machine learning algoritms can work with.
                       
                                          
                   

