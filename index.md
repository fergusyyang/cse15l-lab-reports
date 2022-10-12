# Lab Report Week 1

In week 1 lab, we will learn about how to log into student account on ieng6, using VScode.

First we need to install [VScode](http://code.visualstudio.com/).
Make sure to download the correct version for your computer (Windows/Mac).

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/VScode%20download%20page.png)

Now we want to connect to our SSH remote server.

Before that, we need to use our course-specific account to log into the server.

Here you can look up your [CSE15L account](https://sdacs.ucsd.edu/~icc/index.php).

Reset the password under your account username.

Open VScode. In the tool bar, select Terminal - New Terminal to open a terminal in VScode.

Enter ```ssh cs15lfa22zz@ieng6.ucsd.edu```

(replace "zz" with your account letter, for example, mine is iv)

When asking if you want to connect, enter "yes"

Enter the password to connect with ieng6

(For privacy, what you entered for password will not show up on the screen.)

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/VScode%20terminal.png)

Now, try a few commands in the terminal. 

For example:

* ```cd ~```
* ```cd```
* ```ls```
* ```ls -lat```
* ```ls -a```

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/trying%20commands.png)

You can also move files over SSH with ```scp```.

```scp``` is the command we will use and on your end.

Now we want to create a file on your computer named ```WhereAmI.java```, and move it to the remote server.

Create a java file and type in:

```
class WhereAmI {
  public static void main(String[] args) {
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}
```

In your terminal, compile and run the file

```javac WhereAmI.java```

```java WhereAmI```

Then we will use ```scp``` to move the file over SSH

In the directory where you built ```WhereAmI.java```, enter the following command in your terminal

```scp WhereAmI.java cs15lfa22zz@ieng6.ucsd.edu:~/```

(remember to replace ```zz``` with your username)

After entering your password, you can log into your remote server and check if the file is in the home directory.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/scp2.png)

To ssh or scp without a password, create public key and private key files.

Then ```ssh``` command can use the files instead of having to enter the password.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/ssh%20keys.png)

To have better remote running process, here are some tips:

* use up-arrow to apply the last command
* use semicolon to run multiple commands
* write a command in quote after ssh and id to directly run on ieng6

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/better.png)

[Lab Reports](https://github.com/fergusyyang/cse15l-lab-reports)

[Week 0 Lab Report](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/week-0-lab.md)

