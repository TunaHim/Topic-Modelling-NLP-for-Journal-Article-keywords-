# Topic-Modelling-NLP-for-Journal-Article-keywords-
Extracting Hidden Topics

The objective of the current project is to extract different topics from text using topic modelling techniques. According to the literature, topic modelling is a statistical modeling approach employed in machine learning and natural language processing (NLP) that identifies latent patterns within a collection of texts. This project aims to implement various models to discover and analyze these topics.

To accomplish this, several relevant literatures were reviewed and adapted codes were utilized. The earlier efforts in this domain are duly acknowledged in the references section. The code developed for this project can serve as a prototype for topic modelling using different models. The following steps were followed:
1.	Data Collection: Articles were scraped from the "Frontiers in Renewable Energy" journal, published by "Frontiers." The digital identification number (DOI) of each article was collected from the webpage: https://www.frontiersin.org/journals/energy-research/articles?part-of-research-topic=1. As of March 2023, there were 3395 articles available under the criteria of being "part of research topic." The Title, Publication Date, Abstract, and Keywords of each article were extracted using the BeautifulSoup package and saved as pickle files. Please note that this part is not available in the provided Jupyter file.
2.	Pickle file: For the purpose of simplicity and computational efficiency, only the "keywords" pickle file (keywords.pkl) was used to extract topics. This selection was made considering that the number of keywords is significantly lower than the number of abstract texts.
3.	Data Preprocessing: In the "KeywordsNLP.ipynb" Jupyter file, the required dependencies are imported, and the pickle files are loaded into a dataframe. The data in the dataframe undergoes preprocessing using NLP modules. This involves removing stopwords and irrelevant text, tokenization, stemming, lemmatization, and conversion of the text to term frequency-inverse document frequency (TF-IDF) representation.
4.	Topic Modelling Methods: Several NLP methods were employed for topic modelling, which are briefly described below. For a detailed understanding of these methods, additional information is available on the internet and in the references.
+	Latent Dirichlet Allocation (LDA): LDA was evaluated using coherence scores and visualized with pyLDAvis. The number of topics was limited to six for all the methods, but this can be adjusted based on desired results.
+	Non-Negative Matrix Factorization (NMF): NMF uses the TF-IDF representation as input to the model.
+	Correlation Explanation (CorEx): Similar to NMF, CorEx also utilizes the TF-IDF representation. Both unsupervised and semi-supervised methods are employed for generating topics.
+	Top2Vec: This method utilizes a pre-trained embedding model called "Universal Sentence Encoder," which eliminates the need for preprocessing the texts. It generates its own number of topics, which are visualized in a word cloud. The number of topics can be condensed as per requirements.

By employing these topic modelling techniques, the project aims to uncover hidden patterns and provide insights into the themes present in the journal article keywords.

### References: 
+	Egger R, Yu J. A Topic Modeling Comparison Between LDA, NMF, Top2Vec, and BERTopic to Demystify Twitter Posts. Front Sociol. 2022 May 6;7:886498. doi: 10.3389/fsoc.2022.886498.
+	https://www.machinelearningplus.com/nlp/topic-modeling-gensim-python/#12buildingthetopicmodel 
+	https://www.machinelearningplus.com/nlp/gensim-tutorial/#1introduction
+	https://www.kaggle.com/code/mohitr/topic-modeling-of-paper-abstracts/notebook
+	“How to perform topic modeling with Top2Vec” https://towardsdatascience.com/how-to-perform-topic-modeling-with-top2vec-1ae9bb4e89dc
+	“CorEx Topic Model” https://ryanjgallagher.github.io/code/corex/overview
+	https://medium.com/pew-research-center-decoded/overcoming-the-limitations-of-topic-models-with-a-semi-supervised-approach-b947374e0455
