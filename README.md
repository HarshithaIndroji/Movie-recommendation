# Movie-recommendation
This project focuses on leveraging Natural Language Processing (NLP) techniques and clustering algorithms to identify similarities among movie plot summaries. The first step involves collecting a dataset of movie plot summaries, either from existing sources or from platforms IMDb or Wikipedia. Subsequently, the collected text data undergoes preprocessing. Feature extraction techniques are then employed to convert the textual content into numerical vectors.


Common methods include tokenization, stemming, create TfidfVectorizer enabling the representation of the plot summaries in a format suitable for clustering analysis. The core of the project revolves around clustering algorithm K-Means clustering. These algorithms group together movies with similar plot structures, allowing for the identification of thematic and narrative similarities. The outcome of this project provides a valuable tool for movie enthusiasts, filmmakers, and researchers by offering a systematic approach to explore and understand connections between movies based on their plot summaries. 


We are now ready to implement these concepts. First we’ll import some libraries such as Pandas to manipulate our data, scikit-learn to create our pipeline and train our model and NLTK for natural language for the tokenizer, stopwords and stemming.


The CSV file is loaded into a Pandas DataFrame. The movies dataset have two columns for plot: wiki_plot and imdb_plot. We’ll concatenate they both into a new column called plot so we can have a single column with more information which have the same meaning. In that way, the size of the vocabulary is reduced making it easier for the model to train on a limited dataset. 


Computers can’t process anything but numbers. In order to realize any operations with text, we need first to transform the text to numbers. This process is called vectorization, and as the name suggests, they are organized in vectors. There’s multiple ways of vectorizing text. Here we’ll be using Bag of Words and TF-IDF.


Bag of Words (BoW): Each sentence is represented as a vector with a fixed size equal to the number of words in the vocabulary with each position representing one specific word. The value of this positions is the number of occurences of that specific word in the sentence.


Term Frequency-Inverse Document Frequency(TF-IDF): When we need to compare the similarity between two documents, it’s helpful to assign a measure of importance for each word in the documents, so we can focus on specific parts. 


Product of two terms: The TF term tells the frequency of the word in the document, while the IDF term is about how rarely are documents with that specific word. The basic idea is: If the word appears a lot in very few documents, it must be important. If it appears a lot in many documents, it must not be important(“the”, “of”, “a”, for example). 


So in this way we can use all these techniques and implement the clustering and when it divides into clusters based on the similarity and we can retrieve the movies based on the nearest clusters.
