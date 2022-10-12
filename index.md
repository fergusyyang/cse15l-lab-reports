# Lab Report Week 1

In week 1 lab, we will learn about how to log into student account on ieng6, using VScode.

First we need to install [VScode](http://code.visualstudio.com/).
Make sure to download the correct version for your computer (Windows/Mac).

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/VScode%20download%20page.png)

Open VScode. In the tool bar, select Terminal - New Terminal to open a terminal in VScode.

Enter ssh cs15lfa22zz@ieng6.ucsd.edu

(replace "zz" with your account letter, for example, mine is iv)

When asking if you want to connect, enter "yes"

Enter the password to connect with ieng6

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/VScode%20terminal.png)

Now, try a few commands in the terminal. 

For example:

* cd ~
* cd
* ls
* ls -lat
* ls -a

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/trying%20commands.png)

You can also move files over SSH with scp.

scp is the command we will use and on your end.

We created a file named WhereAmI.java, 

compiled and ran then used scp to move the file over SSH

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/scp2.png)

To ssh or scp without a password, create public key and private key files.

Then ssh command can use the files instead of having to enter the password.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/ssh%20keys.png)

To have better remote running process, here are some tips:

* use up-arrow to apply the last command
* use semicolon to run multiple commands
* write a command in quote after ssh and id to directly run on ieng6

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/better.png)

[Lab Reports](https://github.com/fergusyyang/cse15l-lab-reports)

[Week 1 Lab Report](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/lab-report-1-week-1.md)


[Week 0 Lab Report](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/week-0-lab.md)

