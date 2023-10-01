# NLP
 News Classification Using Naive Bayes Algorithm  
 	NAİVE BAYES
Naive Bayes algorithm is based on Bayes' theorem as shown below and is particularly effective in handling text classification tasks. It assumes that the presence of a particular feature in a class is independent of the presence of other features. Despite this "naive" assumption, Naive Bayes often performs well in practice and is computationally efficient.

P(A\B)=(P(B\A)*P(A))/P(B) 
	P(A|B) = probability of A if B occurs
	P(B|A) = probability of B if A occurs
	P(A) = probability of A
	P(B) = probability of A

In the Scikit-learn library, there are different variations of the Naive Bayes classification algorithm:
BernoulliNB: It is used for binary data sets where features are encoded as 1 if they occur in a specific class, and 0 otherwise.
MultinomialNB: It is used for multi-class classification and counts the frequency of features across classes.
GaussianNB: It is a classification algorithm based on the assumption of normally(Gaussian) distribution, where mean and variance of features are calculated for each class.

Considering its features, the use of GaussianNB was deemed appropriate in this project.


# GAUSSİAN
GaussianNB is a variant of the Naive Bayes algorithm that assumes the likelihood of features to follow a Gaussian distribution. In the context of text classification, each feature can represent a word or a term, and the algorithm models the probability distribution of each class based on the mean and variance of the features in that class. Another advantage of GaussianNB is that it is computationally fast and has low memory requirements. In addition, its ability to give good results even in small data sets has been one of the reasons for preference.

Create the Gaussian Naive Bayes classifier
nb = GaussianNB()

# ALGORITHM IMPLEMENTATION

The implementation of GaussianNB involves several steps:
Data Preprocessing: The text data from the news articles needs to be preprocessed before feeding it into the algorithm. This typically involves steps such as tokenization, removing stopwords, and converting the text into numerical representations suitable for machine learning algorithms.
	Lemmatization: It is a process of make the same words in their stem. For example run, ran, running are different in terms of Python. We lemmatiza the word to get run.
	Stop words: The words that are not important in terms of the context.
	Tokenization: The process of extracting words in a sentence by spaces and punctuations. In this project we'll use nltk's word_tokenize.
	Bag Of Words: BoW is the representation of text data in a numerical way that machine learning algoritms can work with.
 ![image](https://github.com/ozdenozyurt/NLP/assets/112097458/c03189e7-71e9-4ead-818a-e8b4e2e0f2e0)
 ![image](https://github.com/ozdenozyurt/NLP/assets/112097458/9f1c9b6c-30bb-4861-a6e0-72e16e6fd84e)
 ![image](https://github.com/ozdenozyurt/NLP/assets/112097458/12ae3752-73d1-4451-874c-ffb04c25c146)

 # PARAMETERS USED

	TF-ID 
TF-IDF (Term Frequency - Inverse Term Frequency)  is a common technique used for feature weighting in text classification tasks. It assigns weights to words based on their frequency in a document. The vectorizer will calculate the weight of each word in corpus and will return a tf-idf matrix.

W_(i,j)=〖tf〗_(i,j)×log⁡(█(N@-)¦(df_i ))
                                                                                                                                        
	td = Term frequency (number of occurance each i in j)
	df = Document frequency
	N = Number of documents 
	W= tf-idf weight for each i and j (document).


	N GRAM
N-gram models capture the sequential relationships between words or characters in a text. By considering sequences of n consecutive words or characters.  N-gram models can capture local context and dependencies within the text. For example, a bigram model (2-gram) considers pairs of consecutive words. To give an example from the data set, the words in the expression "blood pressure" have different meanings separately, but when evaluated together, they contain a meaning suitable for the medicine category.

# ANALYSIS OF THE RESULTS
As can be seen in below, it has been observed that the accuracy value of the algorithm created is 85%. However, when evaluating such problems, only looking at the accuracy value does not provide an in-depth result, so the values such as recall and f1 score, which are seen in the classification report below, have been issued, and the individual performances of the classes have been determined in the latest confusion matrix.
![image](https://github.com/ozdenozyurt/NLP/assets/112097458/cf123d21-66c0-4dde-abde-97192cd69fc8)
![image](https://github.com/ozdenozyurt/NLP/assets/112097458/e403f8b2-c332-4586-b9e3-22ab75eedb13)






                       
                                          
                   

