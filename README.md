# Malay-Text-Classifier
This repository contains a simple guide to build a Malay text classifier using Scikit-Learn

# Introduction
Text classification refers to the ability of our machine to categorize texts or documents into
different categories based on their content. It is useful across a variety of applications such as
sentiment analysis, email spam classification, automation of products category classification
based on the description, and so on. Text classification has always been an active research in
the community of natural language processing, machine learning and deep learning. However,
most of the research conducted is primarily focused on text classification on English languages.
The performance of text classification by machine in other languages especially Malay is still
poor as compared to English. Therefore, this project will be focused on developing a Malay
Text classifier to perform text classification tasks on Malay documents or texts.

# Text preprocessing
The loaded text might contain some irrelevant information such as symbol, number, url links,
irregular spacing, and so on. These noise elements in text will interfere with the machine
learning algorithm which might reduce the performance and accuracy of the model. Therefore,
some of the useful text preprocessing techniques will be applied into the text dataset before
feeding the text into the machine learning algorithm. Most of the preprocessing steps used will
be involved with the Regular Expression or Regex libraries from python.

**1. Remove all the url inside the text**
To remove url inside a text, the re.sub() method will be used to remove all the
occurrence of substrings that start with “http\S+”” regular expression by replacing it
with an empty string.\
**2. Remove all the non word character**
Some of the text contains non-word characters such as , ^, %, etc that does not hold any
information towards the classification. Therefore, using the re.sub() method again, all
the non-word characters will be replaced by a single space using “\W” regular
expression.\
**3. Remove all the single characters**
Beside non-word characters, some text may also contain irrelevant single characters
such as “I”, “U”,etc from informal text. These single characters will be replaced by a
space using “\s+[a-zA-Z]\s+” regular expression with re.sub() method.\
**4. Replace multiple spaces with single space**
After replacing the single characters with space, the resulting sentence will be
containing multiple unwanted spaces. Therefore, those spaces will also be remove by
substituting the multiple spaces with single space using the “\s+”.\
**5. Convert all words into lowercase**
Next, all the words in texts will be converted into lowercase so that words that have
different cases will be treated equally by the machine learning algorithm. This will be
done by using the standard python.
