# Categorizing Industry on Description #
![Business](https://i.imgur.com/E424NIy.jpg)

## Problem Statement : ## 
### Categorize the Industry in different sectors like Banks, Healthcare,Oil and Natural Gas ###
### I have used LDA to categorize industries based on their description. ###

### What the hell is this LDA now ? ###

LDA : Latent Dirichlet Allocation is an example of topic model and is used to classify text in a
document to a particular topic. It builds a topic per document model and words per topic model, modeled as
Dirichlet distributions.

![Jack Ma](https://i.imgur.com/S9nccoN.jpg)

## Road map ##

1- I observed that all the columns that are in the dataset , do not vary much as per the labels so they are not useful for predictive model

2- Data feature Business Description vary with Industry Classifications so I have chosen this feature.

3- Now If I would be able to get the topic from the business description that could help me tag that industry in particular class

4- Dataset is imbalanced(observed via barplot)

5- Cleaning and tokenizing text :

a- Removing special characters

b- Removing stopwords

c- using [ gensim.utils.simple_preprocess](https://github.com/user/repo/blob/branch/other_file.md) which convert a document into a list of lowercase tokens, ignoring tokens that are too short or too long.

d- Created bigram and trigram [a blog by Dipanjan](https://towardsdatascience.com/understanding-feature-engineering-part-3-traditional-methods-for-text-data-f6f7d70acd41)

[video by me explaining language model](https://www.youtube.com/watch?v=QQOWTtR-ipo)

6- Created a dictionary[gensim.corpora.dictionary](https://radimrehurek.com/gensim/corpora/dictionary.html) which encapsulates the mapping between normalized words and their int

7- Build [LDA model](https://radimrehurek.com/gensim/models/ldamodel.html)

8- Create topics  in LDA model and also view the weightage of keywords in each topic

9- Using [pyLDAvis](https://github.com/bmabey/pyLDAvis) for interactive visualization

10- Achieved [coherence score](https://stats.stackexchange.com/questions/375062/how-does-topic-coherence-score-in-lda-intuitively-makes-sense)
: 0.47945523115286265

11 - Finded optimal number of topics depending on the coherence score

12 - Used [LDA Mallet](https://radimrehurek.com/gensim/models/wrappers/ldamallet.html)which  normally gives better quality of topics

13- Achieved [coherence score](https://stats.stackexchange.com/questions/375062/how-does-topic-coherence-score-in-lda-intuitively-makes-sense):
: 0.5168848885376561)
