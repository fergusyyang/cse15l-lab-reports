# Lab Report Week 1

In week 1 lab, we will learn about how to log into student account on ieng6, using VScode.

As the end of Friday, I was still not able to log in to ieng6 because of password issues, so some screenshots come from groupmates.

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

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/try%20commands.png)

(Screenshot example from Karon Luo)

You can also move files over SSH with scp.

scp is the command we will use and on your end.

We created a file named WhereAmI.java, 

compiled and ran then used scp to move the file over SSH

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/scp.png)

(Screenshot example from Karon Luo)

To ssh or scp without a password, create public key and private key files.

Then ssh command can use the files instead of having to enter the password.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/SSH%20Keys.png)

(Screenshot example from Kailan Luo)

To have better remote running process, here are some tips:

* use up-arrow to apply the last command
* use semicolon to run multiple commands
* write a command in quote after ssh and id to directly run on ieng6

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/Optimizing%20Remote%20Running.png)

(Screenshot example from Kailan Luo)
