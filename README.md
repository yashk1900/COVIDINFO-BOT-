# COVIDINFO-BOT-

COVIDINFOBOT as the name suggests is a chatbot to give you concise information regarding your query about the Corona Virus. 

This chatbot is based on a retrieval-based model and uses the message and context of the conversation for selecting the best response from a predefined list of bot messages.  

Technical Description: 

NLTK and Scikit were the main toolkits used. 

A data source(containing the data about Coronavirus) was used to get all data as text. The ‘Punkt’ tokenizer was used to tokenize the sentences and words.  

Lemmetizer was used to convert all the words to their lemma(basic word from which they were derived). Then TF-IDF(Term Frequency-Inverse Document Frequency) was used to maintain importance of infrequently used words and decrease the importance of the once which occurred many times( as such words don’t always make sense on their own). 

The TF-IDF vectorization converts the tokened sentences to vectors. Then user input was also vectorized. The similarity between vectorized corpus and the vectorized input was calculated using cosine similarity function. The document corresponding to the highest matching was returned. 
