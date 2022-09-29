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


![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/try%20commands.png)

(Screenshot example from Karon Luo)

You can also move files over SSH with scp.

scp is the command we will use. We will run scp on your end.

Try creating a file on your end called WhereAmI.java

and input the following:

class WhereAmI {
  public static void main(String[] args) { 
    System.out.println(System.getProperty("os.name"));
    System.out.println(System.getProperty("user.name"));
    System.out.println(System.getProperty("user.home"));
    System.out.println(System.getProperty("user.dir"));
  }
}

then compile the file using command:

javac WhereAmI.java

and run the file using command:

java WhereAmI

then in the terminal use this scp command with your account:

scp WhereAmI.java cs15lfa22zz@ieng6.ucsd.edu:~/

![Image](https://github.com/fergusyyang/cse15l-lab-reports/blob/main/scp.png)

(Screenshot example from Karon Luo)
