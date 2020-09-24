---
layout: course_inactive
img: cl.png
<!-- img_link: assets/img/neuron.png -->
url_git: https://github.com/uiuc-ling-cl
title: LING402 - LAB05
active_tab: main_page 
---

# LING402: lab05
## Due at 23:59:59 Friday, September 25 2020

* Write a game that prompts the user to guess a word chosen at random from the English Swadesh list:
	* The game should be a Python script which prompts the user for input until the word is guessed correctly
	* Name the script "guess_word.py"
	* All the possible words are contained in the file "words_en"
	* The input prompt should include the number of letters in the word
	* A number representing the number of correct letters in the correct position should be output to stdout after each guess
	* Your code should check the input length, making sure it matches the length of the target word. If the length of input does not match that of the target word, the program should prompt the user for a valid input until it matches.

* Hints:
	* You might wish examine the format of "words_en" by openning it. After reading in the file, one way to go about it is to save all individual words in one list for easy access
	* You can use methods from the "random" module to draw word randomly from the word list built above. You need to decide which exact method(s) in this module to use for your purpose.
	* In order to prompt the number of correct letters in the correct position, you might need to check every character one by one in a guess against the character in the same position in the target word
	* You need a loop to keep the program running until the user hits the correct answer 
	* Same words but in different cases are considered different words, e.g. "Food" is not equal to "food". It would be a good idea to convert both a guess and the target word to upper case or lower case.

* You code should include essential documentations to help others understand what your code does

* You must submit "guess_word.py under the "LAB" diretory in the repository of hw05