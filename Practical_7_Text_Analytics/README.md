```txt id="7n2k4p"
NLP PRACTICAL
TEXT PREPROCESSING USING NLTK

Aim:
To perform text preprocessing and NLP operations using NLTK.

Important Terms:
1. NLP -> Natural Language Processing
2. Tokenization -> Splitting text into words/sentences
3. Stop Words -> Common unnecessary words
4. POS Tagging -> Identifying grammatical roles
5. Stemming -> Reducing words to root form
6. Lemmatization -> Converting words to meaningful base form
7. TF-IDF -> Numerical representation of text
8. Corpus -> Collection of text documents

Code Explanation:

import nltk
Used for Natural Language Processing tasks.

import re
Used for regular expressions and text cleaning.

sent_tokenize
Used for sentence tokenization.

word_tokenize
Used for word tokenization.

stopwords
Provides list of common stop words.

PorterStemmer
Used for stemming.

WordNetLemmatizer
Used for lemmatization.

TfidfVectorizer
Used for TF-IDF representation.

nltk.download('punkt')
Downloads tokenizer package.

nltk.download('stopwords')
Downloads stop words dataset.

nltk.download('wordnet')
Downloads word dictionary for lemmatization.

text = """..."""
Stores input paragraph.

print(text)
Displays original text.

sent_tokenize(text)
Splits paragraph into sentences.

Example:
Sentence 1
Sentence 2

word_tokenize(text)
Splits text into words and punctuation.

re.sub('[^a-zA-Z]', ' ', text)
Removes punctuation and special characters.

[^a-zA-Z]
Means:
Keep only alphabets.

stopwords.words('english')
Loads English stop words.

Examples:
is, the, and, to

filtered_words = [word for word in tokens if word not in stop_words]
Removes stop words from tokens.

nltk.pos_tag(filtered_words)
Performs POS tagging.

POS Tags Examples:
NN -> Noun
VB -> Verb
JJ -> Adjective

PorterStemmer()
Creates stemming object.

ps.stem(word)
Converts word into root form.

Example:
playing -> play

WordNetLemmatizer()
Creates lemmatizer object.

lemmatizer.lemmatize(word)
Converts words into meaningful base form.

Example:
better -> good
cars -> car

documents = [text]
Creates list of documents.

TfidfVectorizer()
Creates TF-IDF vectorizer.

fit_transform(documents)
Calculates TF-IDF values.

TF-IDF:
Term Frequency - Inverse Document Frequency

Used to measure word importance.

get_feature_names_out()
Displays important words/features.

tfidf_matrix.toarray()
Converts sparse matrix into array format.

Important Viva Questions:

Q1. What is NLP?
Answer:
Natural Language Processing.

Q2. What is tokenization?
Answer:
Splitting text into smaller parts.

Q3. Types of tokenization?
Answer:
Sentence tokenization and word tokenization.

Q4. What is sentence tokenization?
Answer:
Splitting paragraph into sentences.

Q5. What is word tokenization?
Answer:
Splitting sentence into words.

Q6. What are stop words?
Answer:
Common unnecessary words.

Q7. Examples of stop words?
Answer:
is, the, and, to

Q8. Why remove stop words?
Answer:
To reduce unnecessary words.

Q9. What is stemming?
Answer:
Reducing words to root form.

Q10. Example of stemming?
Answer:
playing -> play

Q11. What is lemmatization?
Answer:
Converting words into meaningful base form.

Q12. Difference between stemming and lemmatization?
Answer:
Stemming may produce invalid words.
Lemmatization produces meaningful words.

Q13. What is POS tagging?
Answer:
Identifying grammatical roles of words.

Q14. What is TF-IDF?
Answer:
Technique to measure importance of words.

Q15. Full form of TF-IDF?
Answer:
Term Frequency - Inverse Document Frequency.

Q16. What does re.sub() do?
Answer:
Performs text replacement using regex.

Q17. What is regex?
Answer:
Pattern matching technique.

Q18. Which library is used for NLP?
Answer:
NLTK.

Q19. What does fit_transform() do?
Answer:
Learns and transforms data together.

Q20. What is corpus?
Answer:
Collection of text documents.

Q21. Why perform text preprocessing?
Answer:
To clean and prepare text for analysis.

Q22. What is text cleaning?
Answer:
Removing unnecessary characters and words.

Q23. Which function removes punctuation?
Answer:
re.sub()

Q24. What is feature extraction?
Answer:
Converting text into numerical form.

Q25. Why use TF-IDF?
Answer:
To convert text into machine-readable numerical values.

Simple Viva Flow:
1. Imported libraries
2. Loaded text
3. Performed sentence tokenization
4. Performed word tokenization
5. Removed punctuation
6. Removed stop words
7. Applied POS tagging
8. Applied stemming
9. Applied lemmatization
10. Generated TF-IDF representation

Conclusion:
This practical demonstrates text preprocessing techniques and TF-IDF feature extraction using NLTK and Scikit-learn.

```
