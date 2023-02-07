# NLP -> Text Classification using LSTM

Natural Language Processing or NLP is a branch of Artificial Intelligence which deal with bridging the machines understanding humans in their Natural Language. NLP can enable humans to communicate to machines in a natural way.

Text Classification is a process involved in Sentiment Analysis. It is classification of peoples opinion or expressions into different sentiments. Sentiments include Positive, Neutral, and Negative, Review Ratings and Happy, Sad. Sentiment Analysis can be done on different consumer centered industries to analyse people's opinion on a particular product or subject.

I will go through all the key and fundamental concepts of NLP and Sequence Models, which you will get to learn in this repository.

![pic1](https://user-images.githubusercontent.com/35486320/216017228-ecf48fba-6dac-45af-9ded-87c73b727969.png)

## Text Preprocessing

Tweet texts often consists of other user mentions, hyperlink texts, emoticons and punctuations. In order to use them for learning using a Language Model. We cannot permit those texts for training a model. So we have to clean the text data using various preprocessing and cleansing methods. Let's continue

### 1. Stemming/ Lematization

For grammatical reasons, documents are going to use different forms of a word, such as write, writing and writes. Additionally, there are families of derivationally related words with similar meanings. The goal of both stemming and lemmatization is to reduce inflectional forms and sometimes derivationally related forms of a word to a common base form.

**Stemming** usually refers to a process that chops off the ends of words in the hope of achieving goal correctly most of the time and often includes the removal of derivational affixes.

**Lemmatization** usually refers to doing things properly with the use of a vocabulary and morphological analysis of words, normally aiming to remove inflectional endings only and to return the base and dictionary form of a word

![pic2](https://user-images.githubusercontent.com/35486320/216248557-9e9ed24c-a33f-4ab2-9a4c-4055dc5bd7f7.png)

### 2. Hyperlinks and Mentions

Twitter is a social media platform where people can tag and mentions other people's ID and share videos and blogs from internet. So the tweets often contain lots of Hyperlinks and twitter mentions.

### 3. Stopwords

Stopwords are commonly used words in English which have no contextual meaning in an sentence. So therefore we remove them before classification. Some stopwords are...

![pic3](https://user-images.githubusercontent.com/35486320/216248924-9911d867-0d11-499e-8a8f-a6844559d981.png)

### 4. Tokenization

Given a character sequence and a defined document unit, tokenization is the task of chopping it up into pieces, called tokens , perhaps at the same time throwing away certain characters, such as punctuation. The process is called **Tokenization**.

![pic4](https://user-images.githubusercontent.com/35486320/217239796-4d608b98-b108-4b4e-921d-3f18f9e92f89.png)

- `tokenizer` create tokens for every word in the data corpus and map them to a index using dictionary.
- `word_index` contains the index for each word
- `vocab_size` represents the total number of word in the data corpus

### 5. Label Encoding

We are building the model to predict class in enocoded form (0 or 1 as this is a binary classification). We should encode our training labels to encodings.

### 6. Word Emdedding

In Language Model, words are represented in a way to intend more meaning and for learning the patterns and contextual meaning behind it.

**Word Embedding** is one of the popular representation of document vocabulary.It is capable of capturing context of a word in a document, semantic and syntactic similarity, relation with other words, etc.

Basically, it's a feature vector representation of words which are used for other natural language processing applications.

We could train the embedding ourselves but that would take a while to train and it wouldn't be effective. So going in the path of Computer Vision, here we use **Transfer Learning**. We download the pre-trained embedding and use it in our model.

The pretrained Word Embedding like **GloVe & Word2Vec** gives more insights for a word which can be used for classification.
