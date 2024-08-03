# Movie-recommendation
This project focuses on leveraging Natural Language Processing (NLP) techniques and clustering algorithms to identify similarities among movie plot summaries. The first step involves collecting a dataset of movie plot summaries, either from existing sources or from platforms IMDb or Wikipedia. Subsequently, the collected text data undergoes preprocessing. Feature extraction techniques are then employed to convert the textual content into numerical vectors.


Common methods include tokenization, stemming, create TfidfVectorizer enabling the representation of the plot summaries in a format suitable for clustering analysis. The core of the project revolves around clustering algorithm K-Means clustering. These algorithms group together movies with similar plot structures, allowing for the identification of thematic and narrative similarities. The outcome of this project provides a valuable tool for movie enthusiasts, filmmakers, and researchers by offering a systematic approach to explore and understand connections between movies based on their plot summaries. 


We are now ready to implement these concepts. First we’ll import some libraries such as Pandas to manipulate our data, scikit-learn to create our pipeline and train our model and NLTK for natural language for the tokenizer, stopwords and stemming.


The CSV file is loaded into a Pandas DataFrame. The movies dataset have two columns for plot: wiki_plot and imdb_plot. We’ll concatenate they both into a new column called plot so we can have a single column with more information which have the same meaning. In that way, the size of the vocabulary is reduced making it easier for the model to train on a limited dataset. Computers can’t process anything but numbers. In order to realize any operations with text, we need first to transform the text to numbers. This process is called vectorization, and as the name suggests, they are organized in vectors. There’s multiple ways of vectorizing text. Here we’ll be using Bag of Words and TF-IDF.
