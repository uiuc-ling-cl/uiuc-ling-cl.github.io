---
layout: course_inactive
img: cl.png
<!-- img_link: assets/img/neuron.png -->
url_git: https://github.com/uiuc-ling-cl
title: LING402 - LAB01
active_tab: main_page 
---

# LING402: lab01
## Due at 23:59:59 Friday, August 28 2020

* Connect to the cl server using ssh
* On the cl server, use the "git clone" command to check out HW01 if you have not done so. 
* Use the "cd" command to navigate to the HW01 directory
* Use the "git pull" command to download/update the "LAB" directory
* Use the "cd" command to navigate to the "LAB" directory
* In the "LAB" directory, create a file called hello.sh
* Use vi (or emacs) to edit hello.sh.
* The first line of your hello.sh file must be a shebang line that indicates the script should be run using bash.
* When executed, your script should print the message "Hello, world" to standard output
* On line 2 of your script, you must include a one line comment explaining how your script causes "Hello, world" to be printed. This message must be no shorter than 7 words. If the comment is not on line 2, or if your comment is less than 7 words long, you will not receive credit for this part.
* Use chmod to make the file executable
* Run the script to verify that it works
* Use "git add" to add hello.sh
* Use "git commit" with a meaningful commit message.
* Run the "rubric.sh" script to verify that you have completed all parts of the assignment
* Use "git add" to add "grade.tsv"
* Use "git push" to turn in this assignment
