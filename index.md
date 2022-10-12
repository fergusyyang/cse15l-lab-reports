# Lab Report Week 1

In week 1 lab, we will learn about how to log into student account on ieng6, using VScode.

First we need to install [VScode](http://code.visualstudio.com/).

Make sure to download the correct version for your computer (Windows/Mac).

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/VScode%20download%20page.png)

Now we want to connect to our SSH remote server. Before that, we need to use our course-specific account to log into the server.

Here you can look up your [CSE15L account](https://sdacs.ucsd.edu/~icc/index.php).

Reset the password under your account username.

Open VScode. In the tool bar, select Terminal - New Terminal to open a terminal in VScode.

Enter ```ssh cs15lfa22zz@ieng6.ucsd.edu``` (replace "zz" with your account letter, for example, mine is iv)

When asking if you want to connect, enter ```yes```. Enter the password to log into ieng6 server.

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

Then we will use ```scp``` to move the file over SSH.

In the directory where you built ```WhereAmI.java```, enter the following command in your terminal

```scp WhereAmI.java cs15lfa22zz@ieng6.ucsd.edu:~/```

(remember to replace ```zz``` with your username)

After entering your password, you can log into your remote server and check if the file is in the home directory!

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/scp2.png)

To ssh or scp without a password, we will use the program ```ssh-keygen``` to create public key and private key files.

The public key will be copied to the server, and the private key will be stored on the client.

Use the following for setup:

```
# on client (your computer)
$ ssh-keygen
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/joe/.ssh/id_rsa): /Users/joe/.ssh/id_rsa
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /Users/joe/.ssh/id_rsa.
Your public key has been saved in /Users/joe/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:jZaZH6fI8E2I1D35hnvGeBePQ4ELOf2Ge+G0XknoXp0 joe@Joes-Mac-mini.local
The key's randomart image is:
+---[RSA 3072]----+
|                 |
|       . . + .   |
|      . . B o .  |
|     . . B * +.. |
|      o S = *.B. |
|       = = O.*.*+|
|        + * *.BE+|
|           +.+.o |
|             ..  |
+----[SHA256]-----+
```

When it shows ```Enter file in which to save the key```, press ```enter```.

Then, you should be able to use ```ssh``` command to move the files without having to enter the password.

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/ssh%20keys.png)

To have better remote running process, here are some tips:

* use up-arrow to apply the last command
* use semicolon to run multiple commands
* write a command in quote after ssh and id to directly run on ieng6

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/better.png)
