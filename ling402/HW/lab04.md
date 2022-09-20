---
layout: course_inactive
img: cl.png
<!-- img_link: assets/img/neuron.png -->
url_git: https://github.com/uiuc-ling-cl
title: LING402 - LAB04
active_tab: main_page 
---

# LING402: lab04
## Due at 23:59:59 Friday, September 18 2020

* Write a game that prompts the user to guess a number randomly chosen from between 1 and 1000 by the program
	* The game should be a bash script, and named "**guess_number.sh**"
	* The user should have a limited number of guesses (e.g. 10-20). This means after the given number of attempts, the game will terminate with an appropriate message.
	* After each attempt guess, the output of stdout should specify whether the user's guess is too high, too low, or correct. If a guess is incorrect, the game should prompt and wait for next attempt from the user. Otherwise the game terminates with an appropriate message.
	* It would also be good to check that the user has actually input a number as a guess.


* Hints:
	* You can use **$RANDOM** to generate a random number on bash
	* One way to acquire a random number falling into a specific range is to compute the modulus after division between any random number and the upper limit of the target range.
	* You need a loop to keep the program running until either the user hits the correct answer or the number of guesses exceeds the number of allowed attempts.

* You code should include essential documentations to help others understand what your code does

* You must submit "guess_number.sh" under the "LAB" diretory in the repository of hw04
