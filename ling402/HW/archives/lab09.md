---
layout: course_inactive
img: cl.png
<!-- img_link: assets/img/neuron.png -->
url_git: https://github.com/uiuc-ling-cl
title: LING402 - LAB09
active_tab: main_page 
---

# LING402: lab09
## Due at 23:59:59 Friday, Oct 23 2020

* You are going to write a Python script - "synonyms.py" - to find synonyms for words with nltk

* Get the raw text of "English-Latin1" from nltk.corpus.udhr

* You may split the raw text into sentences using the split() function

* Tokenise each sentence using nltk.word_tokenize().

* For each token in a sentence, find a synonym - i.e. the name of the first lemma of the first synset in wordnet of which the token is a member.

* Not every token will be found a synonym. If a token has a synonym, when the synonym is itself, enclose the original token with a pair of round brackets; when the synonym is a different word, replace the original token in the sentence with its synonym in upper cases

* Write each sentences that have been replaced with synonyms to "replaced.txt"; also print out each modified sentence to STDOUT. In both cases, there should be an empty line in between two sentences.

* You wil find it helpful to look through http://www.nltk.org/_modules/nltk/corpus/reader/wordnet.html

* You code should include essential documentations to help others understand what your code does

* You must submit "synonyms.py" under the "LAB" diretory in the repository of hw09