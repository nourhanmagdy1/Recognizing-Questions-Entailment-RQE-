# Recognizing-Questions-Entailment-RQE-
**BACKGROUND AND OBJECTIVE**
One of the challenges in large-scale information retrieval (IR) is to develop domain-specific methods to
answer natural language questions.That is when users tries to search online for an answer to their question
they struggle to navigate through many links and web pages to find a complete sufficient answer.

Despite the availability of numerous sources and datasets for answer retrieval, Question Answering
(QA) remains a challenging problem due to the difficulty of the question understanding and answer
extraction tasks when tackling domain-specific searches. This is due to several factors, such as the lexical
and semantic challenges of domain-specific data that often include advanced argumentation and complex
contextual information, the higher sparseness of relevant information sources, and the more pronounced
lack of similarities between users’ searches.

The objective of the project is to help in building a system to answer questions based on Recognizing
Question Entailment (RQE). This system retrieve answers to a premise question by retrieving entailed
questions that already have associated answers. Therefore, the entailment relation between two questions
is defined as: question A entails question B if every answer to B is also a correct answer to A.

Our main task is to provide solutions to improve the performance of the Question Answering task. By
build a model to measure the entailment score between two questions, this will improve the performance
by retrieving questions with the highest similarity to the proposed one. The second contribution is
a model that can predict the type of the question, It can improve the performance by comparing the
proposed question only with questions with the same type, this will reduce the run time and make the
Question Answering system faster and provide better results. To accomplish this task we will use two
datasets the first one is MedQuAD dataset and the second one is dataset retrieved from the evaluation of
LiveQAMed2017-TestQuestions Dataset.

**Train Data**
For classification task : MedQuAD Dataset
For Regression task: LiveQAMed2017-TestQuestions Dataset

**Test Data**
For classification task : 30% of MedQuAD Dataset
For Regression task: 30% of LiveQAMed2017-TestQuestions Dataset

**Data Preprocessing**
Data preprocessing is an essential step in building a Machine Learning model and depending on how well
the data has been preprocessed, the results are seen. At the first we removed punctuation like (.,!*”@’)
by selecting pattern of the text that we want and neglect others then convert all characters to lowercase.
Second step we removed stopwords from the text by NLTK library as they don’t add any value to the
analysis like [’am’, ’is’, ’are’, ’does’, ’has’, ’not’, ’or’ and etc.]. Based on the medical dataset we selected
some stopwords and did not remove them like [’who’, ’what’, ’when’, ’why’, ’how’, ’which’, ’where’,
’whom’], because they make a different in the meaning of the medical questions. We applied lemmatizing
or diminished text to the root form and makes sure that it doesn’t lose its meaning by WordNetLemmatizer.
After all the text processing steps are performed, the final acquired data is converted into the numeric
form using TF-IDF transformer, we applied it during pipeline of the model.

**Approaches**
For classification task we used two models to compare between the performance of each one.
For the evaluation we used metrics, accuracy, percision and recall.
For regression task we tried to use machine learning model and deep learning model.
