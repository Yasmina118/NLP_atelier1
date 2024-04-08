# NLP_atelier1
This lab report details the exploration of techniques for scraping Arabic web data, constructing an NLP pipeline for processing the scraped text, and performing named entity recognition (NER).

Steps

Web Scraping with Beautiful Soup
Target website: https://ibtekr.org/
Employed Beautiful Soup to extract relevant content using appropriate selectors.
Stored the scraped data in its raw format.
Raw Data Storage in MongoDB
A MongoDB instance was set up to store the scraped data in a structured format.
A schema was designed to represent the data within MongoDB collections.
A Python driver (e.g., PyMongo) was used for connecting to MongoDB and storing the scraped data.
NLP Pipeline Establishment

a. Text Cleaning

Applied Unicode normalization for consistent character encoding.
Removed emojis, other English text, and unwanted symbols using regular expressions.
Tokenized the text into individual words or meaningful units.
Removed stop words from the Arabic language using arabic_stopwords = set(stopwords.words('arabic')) from the NLTK library.
b. Stemming and Lemmatization

Explored stemming using the ISRIStemmer from NLTK (from nltk.stem import ISRIStemmer) to reduce words to their base forms.
Investigated lemmatization using import qalsadi.lemmatizer for a more linguistically accurate reduction of words to their lemmas.
c. Parts of Speech (POS) Tagging

Examined both rule-based and machine learning approaches for POS tagging.
Considered using the Java Stanford POS tagger.
Named Entity Recognition (NER)

Explored techniques to identify and classify named entities (e.g., people, organizations, locations) within the processed text.
Considered libraries like spaCy with its built-in NER models or NLTK for implementing rule-based or statistical NER approaches.
