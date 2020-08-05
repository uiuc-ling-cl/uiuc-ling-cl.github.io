---
layout: course_inactive
img: cl.png
<!-- img_link: assets/img/neuron.png -->
url_git: https://github.com/uiuc-ling-cl
title: LING402 - LAB 01
active_tab: main_page 
---

# Lab 01

<!--
<div class="alert alert-info">
  Due Tuesday 29 August 2017 at 11:59 PM Central time.
</div>
-->

Do the following:

* Sign up for a [Github username](https://github.com/join?source=header-home)
* Open a [terminal](https://en.wikipedia.org/wiki/Terminal_emulator). On Mac OS X, this will be a program called [Terminal](https://en.wikipedia.org/wiki/Terminal_(OS_X)) in your Applications/Utilities folder. On Windows, you will likely need to download and set up a third-party program such as [PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html). On Linux, this will be the [GNOME Terminal](https://en.wikipedia.org/wiki/GNOME_Terminal) or [KDE Konsole](https://en.wikipedia.org/wiki/Konsole), or [the equivalent](https://en.wikipedia.org/wiki/List_of_terminal_emulators).
* At the [command line](https://en.wikipedia.org/wiki/Command-line_interface) within the terminal emulator, connect to the cl.linguistics.illinois.edu server using [ssh](http://linuxcommand.org/man_pages/ssh1.html). Your username is your NetID, and your password should be your [NetID password](https://techservices.illinois.edu/services/netid-password). Note: to connect to the server from off campus, you may first need to connect to the campus network using an approved [VPN client](https://techservices.illinois.edu/services/virtual-private-networking-vpn/download-and-set-up-the-vpn-client).

```bash
ssh yourActualNetID@cl.linguistics.illinois.edu
```

* At the command line on the cl.linguistics.illinois.edu server, type the following command to create the file ~/.who\_am\_I 

```bash
echo -e "WWW\tXXX\tYYY\tZZZ" > ~/.who_am_I
```

* Use [cat](http://linux.die.net/man/1/cat) to verify that you have successfully saved your changes to .who\_am\_I

```bash
cat ~/.who_am_I
```

You should see this:

>WWW	XXX	YYY	ZZZ


* At the command line on the cl.linguistics.illinois.edu server, use the [vi text editor](http://www.howtogeek.com/102468/a-beginners-guide-to-editing-text-files-with-vi/) to open the file ~/.who\_am\_I 

```bash
vi ~/.who_am_I
```

* Within the vi text editor, [enter insert mode](http://www.howtogeek.com/102468/a-beginners-guide-to-editing-text-files-with-vi/) 

```vi
i
```

* Replace WWW with your [last name](https://en.wikipedia.org/wiki/Surname)
* Replace XXX with your [first name](https://en.wikipedia.org/wiki/Given_name)
* Replace YYY with your [netID](https://netidclaim.illinois.edu/)
* Replace ZZZ with your [Github username](https://github.com/join?source=header-home)
* Within the vi text editor, [exit insert mode](http://www.howtogeek.com/102468/a-beginners-guide-to-editing-text-files-with-vi/) by pressing the Escape key on your keyboard
* [Save your changes](http://www.howtogeek.com/102468/a-beginners-guide-to-editing-text-files-with-vi/) to the file

```
:w
```

* [Exit vi](http://www.howtogeek.com/102468/a-beginners-guide-to-editing-text-files-with-vi/)

```
:q
```


* Use [cat](http://linux.die.net/man/1/cat) to verify that you have successfully saved your changes to .who\_am\_I

```bash
cat ~/.who_am_I
```

You should see something like this (except with your name and IDs):

>Schwartz	Lane	lanes	dowobeha




* Use [cat](http://linux.die.net/man/1/cat), [tail](http://linux.die.net/man/1/tail), [cut](http://linux.die.net/man/1/cut), and [pipes](http://ryanstutorials.net/linuxtutorial/piping.php#piping) to verify that you have successfully recorded your [first name](https://en.wikipedia.org/wiki/Given_name) in .who\_am\_I

```bash
cat ~/.who_am_I | tail -n 1 | cut -f 2
```

You should see something like this (except with your first name):

>Lane

* Use [cat](http://linux.die.net/man/1/cat), [tail](http://linux.die.net/man/1/tail), [cut](http://linux.die.net/man/1/cut), and [pipes](http://ryanstutorials.net/linuxtutorial/piping.php#piping) to verify that you have successfully recorded your [last name](https://en.wikipedia.org/wiki/Surname) in .who\_am\_I

```bash
cat ~/.who_am_I | tail -n 1 | cut -f 1
```

You should see something like this (except with your last name):

>Schwartz


* Use [cat](http://linux.die.net/man/1/cat), [tail](http://linux.die.net/man/1/tail), [cut](http://linux.die.net/man/1/cut), and [pipes](http://ryanstutorials.net/linuxtutorial/piping.php#piping) to verify that you have successfully recorded your [github](https://github.com) username in .who\_am\_I

```bash
cat ~/.who_am_I | tail -n 1 | cut -f 4
```

You should see something like this (except with your Github ID):

>dowobeha

* Use [cat](http://linux.die.net/man/1/cat), [tail](http://linux.die.net/man/1/tail), [cut](http://linux.die.net/man/1/cut), and [pipes](http://ryanstutorials.net/linuxtutorial/piping.php#piping) to verify that your NetID is still correctly recorded your in .who\_am\_I

```bash
cat ~/.who_am_I | tail -n 1 | cut -f 3
```

You should see something like this (except with your netID):

>lanes

```bash
cat ~/.who_am_I | tail -n 1 | tr '\t' '\n' | wc -l
```

You should see exactly this:

>4

If you see anything other than 4, or if any of the previous validation steps don't match what you actually see, you have a problem with your file, and you will not receive credit for the assignment. The most common problem is the use of spaces instead of tabs. You must use tabs, not spaces, to separate the entries in the file.


* Disconnect from the server

```bash
exit
```

